<template>
  <div class="hero">
    <mdb-view src class="h-100">
      <mdb-mask
        overlay="black-strong"
        color="#78909c"
        class="d-flex justify-content-center align-items-center"
      >
        <mdb-container>
          <mdb-row>
            <mdb-col md="12" class="text-center">
              <h1 class="h1-reponsive white-text code">
                <strong>
                  <span class="d-inline-flex">Cameron Michael Nickert</span>
                  <span class="pink-text" style="font-size: 1rem;">{{getDegreeStatus}}</span>
                </strong>
              </h1>
              <h5 class="code pink-text">
                <span class="d-inline-flex">Full-Time Software Engineer</span>
              </h5>
              <hr class="hr-light mt-4" />
              <div class="mb-5 text-white" style="height: 4em;">
                <span class="code">{{message}}</span>
                <span class="animated flash infinite">|</span>
              </div>
              <div class="pink-text h1 pt-5 mt-5 animated fadeInUp slower delay-4s">
                <i class="fas fa-chevron-down animated bounce slower infinite delay-5s"></i>
              </div>
            </mdb-col>
          </mdb-row>
        </mdb-container>
      </mdb-mask>
    </mdb-view>
  </div>
</template>

<script>
import {
  mdbContainer,
  mdbRow,
  mdbCol,
  mdbMask, //mdbBtn,
  mdbView
} from "mdbvue";
export default {
  name: "Hero",
  components: {
    mdbContainer,
    mdbRow,
    mdbCol,
    mdbMask,
    //mdbBtn,
    mdbView
  },
  data: () => {
    return { message: "" };
  },
  created: function() {
    let phrase = "Empowering the world with one line of code at a time;";

    this.startTypewriter(phrase);

    setInterval(() => {
      this.restartTypewriter(phrase);
    }, 15000);
  },
  computed: {
    getDegreeStatus: function() {
      let graduationDate = new Date("12/12/2020");
      let todaysDate = new Date();
      if (todaysDate.getTime() > graduationDate.getTime()) {
        return "M.S.";
      } else {
        return "B.S.";
      }
    }
  },
  methods: {
    startTypewriter: function(phrase) {
      if (phrase.length > this.message.length) {
        setTimeout(() => {
          this.message += phrase.charAt(this.message.length);
          this.startTypewriter(phrase);
        }, 100);
      }
    },
    restartTypewriter: function(phrase) {
      if (this.message.length > 0) {
        setTimeout(() => {
          this.message = this.message.slice(0, -1);
          this.restartTypewriter(phrase);
        }, 20);
      } else {
        setTimeout(() => {
          this.startTypewriter(phrase);
        }, 1000);
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.btn-circle {
  border-radius: 5em;
  height: 5em;
  width: 5em;
  display: inline-flex;
  justify-content: center;
}

.hero {
  height: calc(100vh - 60px);
}

.hero .view {
  background-image: url(../../assets/stock_computer.jpeg);
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}

.hero .gradient {
  background: -webkit-linear-gradient(
    45deg,
    rgba(0, 0, 0, 0.7),
    rgba(72, 15, 144, 0.4) 100%
  );
  background: linear-gradient(
    45deg,
    rgba(0, 0, 0, 0.7),
    rgba(72, 15, 144, 0.4) 100%
  );
}

.hero .card {
  background-color: rgba(126, 123, 215, 0.2);
}

.hero h6 {
  line-height: 1.7;
}

.hero .navbar {
  transition: background 0.5s ease-in-out, padding 0.5s ease-in-out;
}

.hero .navbar .md-form {
  margin: 0;
}

.top-nav-collapse {
  background: #424f95 !important;
}

@media (max-width: 768px) {
  .hero .navbar:not(.top-nav-collapse) {
    background: #424f95 !important;
  }
}

.hero label {
  color: #fff !important;
}
</style>
