<template>
  <div class="sf-services">
    <div class="container">
      <div class="text-button">
        <h3 class="heading">
          We offer end-to-end customs services with fast, accurate and compliant
          customs in multiple countries
        </h3>
        <template>
          <button
            class="color-primary sf-button get-touch-button"
            :aria-disabled="false"
            :link="null"
            type="button"
            aria-label="button"
          >
            Get in touch
          </button>
        </template>
      </div>
      <div class="bottom-divider"></div>

      <div class="cards-row">
        <div class="card">
          <img src="../assets/images/icons/Komponente 10 – 1.png" alt="" />
          <h3 class="heading-text">Fast and accurate</h3>
          <p class="subtitle">
            We offer you a full-service offering with fast and accurate customs
            in multiple countries.
          </p>
        </div>
        <div v-show="screenWidth" class="card">
          <img src="../assets/images/icons/Komponente 11 – 1.png" alt="" />
          <h3 class="heading-text">Strict compliance</h3>
          <p class="subtitle">
            We make sure you are compliant with regulations to mitigate
            customs-related risk and exposure.
          </p>
        </div>
        <div v-show="screenWidth" class="card">
          <img src="../assets/images/icons/Komponente 12 – 1.png" alt="" />
          <h3 class="heading-text">Qualified professionals</h3>
          <p class="subtitle">
            Our highly skilled professionals offer customs expert advice to
            optimise your duty management and help you save costs.
          </p>
        </div>
        <div v-show="!screenWidth" class="icons-area">
          <div class="icons">
            <img src="../assets/images/icons/Ellipse 115.png" alt="" />
            <img src="../assets/images/icons/Ellipse 116.png" alt="" />
            <img src="../assets/images/icons/Ellipse 116.png" alt="" />
            <img src="../assets/images/icons/Ellipse 116.png" alt="" />
            <img src="../assets/images/icons/Ellipse 116.png" alt="" />
            <img src="../assets/images/icons/Ellipse 116.png" alt="" />
          </div>
          <div class="icons-sec">
            <span
              ><img src="../assets/images/icons/Gruppe 474.png" alt=""
            /></span>
            <span
              ><img src="../assets/images/icons/Gruppe 520.png" alt=""
            /></span>
          </div>
        </div>
      </div>

      <div v-show="screenWidth" class="cards-row">
        <div class="card">
          <img src="../assets/images/icons/Komponente 13 – 1.png" alt="" />
          <h3 class="heading-text">Online and real-time control</h3>
          <p class="subtitle">
            Real-time compliance and finance dashboards to manage your customer
            portfolio.
          </p>
        </div>
        <div class="card">
          <img src="../assets/images/icons/Komponente 14 – 1.png" alt="" />
          <h3 class="heading-text">EU-wide coverage</h3>
          <p class="subtitle">
            We have offices in 5 European countries, but thanks to our network
            of trusted partners we have EU-wide coverage.
          </p>
        </div>
        <div class="card">
          <img src="../assets/images/icons/Komponente 15 – 1.png" alt="" />
          <h3 class="heading-text">Fast and accurate</h3>
          <p class="subtitle">
            We offer you a full-service offering with fast and accurate customs
            in multiple countries.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { SfHeader, SfIcon, SfCarousel } from "@storefront-ui/vue";
import { defineComponent } from "@nuxtjs/composition-api";

export default defineComponent({
  components: {
    SfHeader,
    SfIcon,
    SfCarousel,
  },

  data() {
    return {
      screenWidth: true,
    };
  },

  mounted() {
    this.$nextTick(() => {
      window.addEventListener("resize", this.onResize);
    });
  },

  beforeDestroy() {
    window.removeEventListener("resize", this.onResize);
  },

  methods: {
    onResize() {
      if (window.innerWidth < 1024) {
        this.screenWidth = false;
      } else {
        this.screenWidth = true;
      }
    },
  },
});
</script>

<style lang="scss" scoped>
.sf-services {
  padding: 100px 0;

  .container {
    max-width: 1270px;
    margin: 0 auto;

    .text-button {
      display: flex;
      align-items: center;
      justify-content: space-between;

      @media (max-width: 1024px) {
        flex-direction: column;
        padding-left: 35px;
      }

      .heading {
        font-size: 30px;
        color: #3d4d62;
        padding-right: 40px;

        @media (max-width: 1024px) {
          font-size: 25px;
        }
      }
    }

    .bottom-divider {
      width: 50px;
      height: 3px;
      border-radius: 20px;
      margin-top: 30px;
      background-color: #01a4b7;

      @media (max-width: 1024px) {
        margin-left: 35px;
      }
    }

    .cards-row {
      display: flex;
      align-items: center;
      gap: 20px;
      @media (max-width: 1024px) {
        flex-direction: column;
        align-items: flex-start;
      }

      .card {
        width: 33%;
        padding-top: 40px;

        @media (max-width: 1024px) {
          padding-left: 20px;
          width: 100%;
        }

        .heading-text {
          font-size: 20px;
          font-weight: bold;
          color: #3d4d62;
          margin-top: 15px;
        }

        .subtitle {
          font-size: 16px;
          font-weight: 400;
          color: #3d4d62;
          padding-right: 44px;
          line-height: 22px;
          display: flex;
          flex-direction: column;
          align-items: baseline;
          max-height: 40px;
        }

        &:hover {
          img {
            margin-left: 10px;
            transition: all ease 0.4s;
          }
          .heading-text {
            color: #01a4b7;
          }
        }
      }

      .icons-area {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        margin-top: 30px;

        .icons {
          margin-left: 20px;
        }

        .icons-sec {
          margin-right: 20px;
        }
      }
    }
  }
}
</style>
