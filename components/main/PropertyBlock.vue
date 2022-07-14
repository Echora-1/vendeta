<template>
  <div class="container property-block">
    <property-card v-for="(card, index) in $t('cards')" :key="index" class="property-block__card" :content="card"  />
  </div>
</template>

<i18n>
{
  "en": {
    "cards": [
      {
        "img": "payment",
        "title": "Nanopayment Ecosystem",
        "text": "Try to a new probabilistic nanopayment system to scale payment throughput via cryptocurrency-backed “tickets”."
      },
      {
        "img": "decentralised",
        "title": "Decentralised",
        "text": "VENDETA empowers you to regain your internet privacy and stay invisible from all kinds of surveillance and censorship."
      },
      {
        "img": "node",
        "title": "Node Competition",
        "text": "Run a node from your own home and get paid to share your excess internet resources with those who need it."
      }
    ]
  },
  "ch": {
    "cards": [
      {
        "img": "payment",
        "title": "Nanopayment Ecosystem",
        "text": "Try to a new probabilistic nanopayment system to scale payment throughput via cryptocurrency-backed “tickets”."
      },
      {
        "img": "decentralised",
        "title": "Decentralised",
        "text": "VENDETA empowers you to regain your internet privacy and stay invisible from all kinds of surveillance and censorship."
      },
      {
        "img": "node",
        "title": "Node Competition",
        "text": "Run a node from your own home and get paid to share your excess internet resources with those who need it."
      }
    ]
  },
  "tur": {
    "cards": [
      {
        "img": "payment",
        "title": "Nanopayment Ecosystem",
        "text": "Try to a new probabilistic nanopayment system to scale payment throughput via cryptocurrency-backed “tickets”."
      },
      {
        "img": "decentralised",
        "title": "Decentralised",
        "text": "VENDETA empowers you to regain your internet privacy and stay invisible from all kinds of surveillance and censorship."
      },
      {
        "img": "node",
        "title": "Node Competition",
        "text": "Run a node from your own home and get paid to share your excess internet resources with those who need it."
      }
    ]
  }
}
</i18n>

<script>
import PropertyCard from '~/components/main/PropertyCard'
export default {
  components: { PropertyCard },
}
</script>

<style lang="scss" scoped>
.property-block {
  display: flex;

  &__card {
    max-width: calc((1240px - 64px) / 3);
    width: 100%;

    &:not(:first-child) {
      margin-left: 32px;
    }
  }
}
</style>
