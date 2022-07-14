<template>
  <div class="container reviews-block">
    <h2 class="base-title">Reviews</h2>
    <div class="reviews-block__list">
      <client-only>
        <Flickity id='reviews-carousel' ref="flickity" :key='sliderKey' :options="flickityOptions">
          <reviews-card v-for="(card, index) in $t('cards')" :key="index" :content="card" class="reviews-block__item" />
        </Flickity>
      </client-only>
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "cards": [
      {
        "text": "“Excellent VPN and so easy to use. Has an ever-growing list of countries to choose from.”",
        "name": "Brian Aubin",
        "rating": 5
      },
      {
        "text": "“Much faster and better user interface than my previous vpn. Exceptional value for money - go for it!”",
        "name": "Clark",
        "rating": 5
      },
      {
        "text": "“I am so happy with customer support, Harvey saved my evening, fast and clear, thank you.”",
        "name": "Javeline",
        "rating": 5
      },
      {
        "text": "“Excellent VPN and so easy to use. Has an ever-growing list of countries to choose from.”",
        "name": "Brian Aubin",
        "rating": 5
      },
      {
        "text": "“Much faster and better user interface than my previous vpn. Exceptional value for money - go for it!”",
        "name": "Clark",
        "rating": 5
      },
      {
        "text": "“I am so happy with customer support, Harvey saved my evening, fast and clear, thank you.”",
        "name": "Javeline",
        "rating": 5
      }
    ]
  },
  "ch": {
    "cards": [
      {
        "text": "“Excellent VPN and so easy to use. Has an ever-growing list of countries to choose from.”",
        "name": "Brian Aubin",
        "rating": 5
      },
      {
        "text": "“Much faster and better user interface than my previous vpn. Exceptional value for money - go for it!”",
        "name": "Clark",
        "rating": 5
      },
      {
        "text": "“I am so happy with customer support, Harvey saved my evening, fast and clear, thank you.”",
        "name": "Javeline",
        "rating": 5
      },
      {
        "text": "“Excellent VPN and so easy to use. Has an ever-growing list of countries to choose from.”",
        "name": "Brian Aubin",
        "rating": 5
      },
      {
        "text": "“Much faster and better user interface than my previous vpn. Exceptional value for money - go for it!”",
        "name": "Clark",
        "rating": 5
      },
      {
        "text": "“I am so happy with customer support, Harvey saved my evening, fast and clear, thank you.”",
        "name": "Javeline",
        "rating": 5
      }
    ]
  },
  "tur": {
    "cards": [
      {
        "text": "“Excellent VPN and so easy to use. Has an ever-growing list of countries to choose from.”",
        "name": "Brian Aubin",
        "rating": 5
      },
      {
        "text": "“Much faster and better user interface than my previous vpn. Exceptional value for money - go for it!”",
        "name": "Clark",
        "rating": 5
      },
      {
        "text": "“I am so happy with customer support, Harvey saved my evening, fast and clear, thank you.”",
        "name": "Javeline",
        "rating": 5
      },
      {
        "text": "“Excellent VPN and so easy to use. Has an ever-growing list of countries to choose from.”",
        "name": "Brian Aubin",
        "rating": 5
      },
      {
        "text": "“Much faster and better user interface than my previous vpn. Exceptional value for money - go for it!”",
        "name": "Clark",
        "rating": 5
      },
      {
        "text": "“I am so happy with customer support, Harvey saved my evening, fast and clear, thank you.”",
        "name": "Javeline",
        "rating": 5
      }
    ]
  }
}
</i18n>

<script>
import ReviewsCard from "~/components/main/ReviewsCard";
export default  {
  components: {ReviewsCard},

  data() {
    return {
      innerWidth: 0,
      sliderKey: 1,
    }
  },

  computed: {
    flickityOptions() {
      if( this.innerWidth > 767 && this.innerWidth < 1200) {
        return {
          pageDots: true,
          wrapAround: false,
          groupCells: 2,
          prevNextButtons: false
        }
      }
      if(this.innerWidth <= 767) {
        return {
          pageDots: true,
          wrapAround: false,
          groupCells: 1,
          prevNextButtons: false
        }
      }
      return {
        pageDots: true,
        wrapAround: false,
        groupCells: 3,
        prevNextButtons: false
      }
    }
  },

  watch: {
    flickityOptions() {
      this.sliderKey += 1
    }
  },

  mounted() {
    this.setWidth();
    window.addEventListener('resize', this.setWidth);
  },

  methods: {
    setWidth() {
      this.innerWidth = window.innerWidth
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  max-width: 1312px;
}

.reviews-block {
  display: flex;
  align-items: center;
  flex-direction: column;

  &__list {
    width: 100%;
    max-width: 380px;

    @media (min-width: 768px) {
      max-width: 760px
    }

    @media (min-width: 1200px) {
      max-width: 100%;
    }
  }

  &__item {
    margin-right: 32px;
    width: calc((100% - 32px));

    @media (min-width: 768px) {
      width: calc((100% - 64px) / 2);
    }

    @media (min-width: 1200px) {
      width: calc((1272px - 96px) / 3);
    }
  }
}
</style>
