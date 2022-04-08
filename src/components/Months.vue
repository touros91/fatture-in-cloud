<template>
  <div class="container">
    <!-- months  -->
    <div class="months">
      <div class="month" v-for="month in months" :key="month">
        {{ month }}
      </div>
    </div>
    <!-- monthly stats  -->
    <div class="month-container" id="selectable">
      <div
        @click="
          selected = months[index];
          details = { importo: data.importo, documenti: data.documenti };
        "
        class="stats"
        v-for="(data, index) in data.data"
        :key="index"
      >
        <div
          class="bg-green"
          :style="{ top: 81 - data.importo / 1000 + 'px' }"
        ></div>

        <span class="doc">{{ data.documenti }} doc.</span>
        <span class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </span>
      </div>
    </div>

    <div v-if="selected">
      <h1>{{ selected }}</h1>
      <p>Documenti disponibili per questo mese: {{ details.documenti }}</p>

      <p>
        L'importo totale è:
        {{
          new Intl.NumberFormat("de-DE", {
            style: "currency",
            currency: "EUR",
          })
            .format(details.importo)
            .toLocaleString()
            .replace(/,00/g, " ")
        }}
      </p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      data: null,
      months: [
        "Gennaio",
        "Febbraio",
        "Marzo",
        "Aprile",
        "Maggio",
        "Giugno",
        "Luglio",
        "Agosto",
        "Settembre",
        "Ottobre",
        "Novembre",
        "Dicembre",
      ],
      selected: "",
      details: {},
    };
  },
  created() {
    // API call using axios to retrieve data from db.json
    axios.get("http://localhost:3000/mesi").then((response) => {
      this.data = response;
      console.log(response);
    });
  },
};
</script>

<style>
#selectable .ui-selecting :not(span) {
  border-bottom: 3px solid #7abdd9;
}
#selectable .ui-selected :not(span) {
  border-bottom: 4px solid #0a97d5;
}

.container {
  font-size: 12px;
  max-width: 1200px;
  margin: 0 auto;
}

.months {
  display: flex;
}

.month-container {
  display: flex;
  justify-content: space-between;
  border: 1px solid #ecedee;
  position: relative;
  border: none;
}

.stats {
  width: 110px;
  height: 81px;
  display: flex;
  flex-direction: column;
  line-height: 18px;
  justify-content: flex-end;
  position: relative;
  border-bottom: 1px solid #ecedee;
  border-right: 1px solid #ecedee;
  cursor: pointer;
}

.bg-green {
  content: "";
  width: 100%;
  background: #dff1ea;
  position: absolute;
  top: 0;
  bottom: 0;
}

.month {
  border-bottom: 1px solid #ecedee;
  border-top: 1px solid #ecedee;
  border-right: 1px solid #ecedee;
  padding: 5px;
  color: #0a97d5;
  display: inline-block;
  width: 100px;
}

.month:first-child,
.stats:first-child {
  border-left: 1px solid #ecedee;
}

.doc {
  padding: 5px;
  z-index: 1;
  color: #6f7e86;
}

.amount {
  color: #00875a;
}

h1 {
  margin: 60px 0 30px 0;
}

p {
  font-size: 15px;
}
</style>