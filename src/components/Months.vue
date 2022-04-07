<template>
  <div class="container">
    <div class="month-container bg">
      <div class="month">Gennaio</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[0].importo / 1000 + 'px' }"
        ></div>

        <div class="doc">{{ data.data[0].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[0].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Febbraio</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[1].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[1].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[1].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Marzo</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[2].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[2].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[2].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Aprile</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[3].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[3].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[3].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Maggio</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[4].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[4].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[4].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Giugno</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[5].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[5].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[5].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Luglio</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[6].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[6].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[6].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Agosto</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[7].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[7].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[7].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Settembre</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[8].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[8].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[8].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Ottobre</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[9].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[9].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[9].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Novembre</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[10].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[10].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[10].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
    <div class="month-container">
      <div class="month">Dicembre</div>
      <div class="stats">
        <div
          class="bg-green"
          :style="{ top: 81 - data.data[11].importo / 1000 + 'px' }"
        ></div>
        <div class="doc">{{ data.data[11].documenti }} doc.</div>
        <div class="doc amount">
          {{
            new Intl.NumberFormat("de-DE", {
              style: "currency",
              currency: "EUR",
            })
              .format(data.data[11].importo)
              .toLocaleString()
              .replace(/,00/g, " ")
          }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      data: null,
    };
  },
  created() {
    axios.get("http://localhost:3000/mesi").then((response) => {
      this.data = response;
      console.log(response);
    });
  },
};
</script>

<style>
.container {
  display: flex;
  justify-content: center;
  font-size: 12px;
}

.month-container {
  width: 100px;
  border: 1px solid #ecedee;
  position: relative;
  border: none;
}

.month-container:active {
  border-bottom: 4px solid red;
}

.stats {
  height: 81px;
  display: flex;
  flex-direction: column;
  line-height: 18px;
  justify-content: flex-end;
  position: relative;
}

.bg-green {
  content: "";
  min-width: 100px;
  background: #dff1ea;
  position: absolute;
  top: 0;
  bottom: 0;
  /* right: 0; */
  /* left: 0; */
}

.month {
  border-bottom: 1px solid #ecedee;
  padding: 5px;
  color: #0a97d5;
}

.doc {
  padding: 5px;
  z-index: 1;
  color: #6f7e86;
}

.amount {
  color: #00875a;
}

/* .border-bottom {
  position: absolute;
  height: 3px;
  left: 0px;
  right: 0px;
  bottom: 0px;
} */
</style>