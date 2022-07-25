<template>
  <div class="container system-block">
    <div class="system-block__left">
      <img src="../../assets/img/system.svg" class="system-block__img" width="601" height="431" alt="system" />
    </div>
    <div class="system-block__right">
      <h2 class="base-title">{{ $t('title') }}</h2>
      <p class="base-subtitle">
        {{ $t('subtitle')[0] }}<br /><br />
        {{ $t('subtitle')[1] }}
      </p>
      <ul>
        <li v-for="(li, index) in $t('list')" :key="index" class="base-list-item">
          <span>{{ li }}</span
          >
        </li>
      </ul>
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "title": "Meet VEN system",
    "subtitle": ["Privacy — meets P2P VPN. Try out to redefine what it means to be connected through people-powered protocols. No central points of failure or control.", "Browse anonymously and leave absolutely no trace."],
    "list": ["Pay for VPN service using one of our supported cryptocurrencies.", "Instant, on-demand settlement.", "Low operational and liquidity costs."]
  },
  "ch": {
    "title": "Meet VEN system",
    "subtitle": ["Privacy — meets P2P VPN. Try out to redefine what it means to be connected through people-powered protocols. No central points of failure or control.", "Browse anonymously and leave absolutely no trace."],
    "list": ["Pay for VPN service using one of our supported cryptocurrencies.", "Instant, on-demand settlement.", "Low operational and liquidity costs."]
  },
  "tur": {
    "title": "Meet VEN system",
    "subtitle": ["Privacy — meets P2P VPN. Try out to redefine what it means to be connected through people-powered protocols. No central points of failure or control.", "Browse anonymously and leave absolutely no trace."],
    "list": ["Pay for VPN service using one of our supported cryptocurrencies.", "Instant, on-demand settlement.", "Low operational and liquidity costs."]
  }
}
</i18n>

<style lang="scss" scoped>
.base-title {
  margin-bottom: 12px;
}

.base-subtitle {
  margin: 0;
  max-width: 550px;
}

.system-block {
  display: flex;

  @media(max-width: 767px) {
    flex-direction: column-reverse;
  }

  &__left,
  &__right {
    @media(min-width: 768px) {
      flex: 0 0 50%;
      max-width: 50%;
    }
  }

  &__left {
    @media(min-width: 768px) {
      padding-right: 16px;
    }
  }

  &__right {
    @media(min-width: 768px) {
      padding-left: 16px;
      padding-top: 25px;
    }
  }

  &__img {
    width: 100%;
    height: 100%;
    max-width: 601px;
    max-height: 431px;

    @media(max-width: 767px) {
      transform: scale(1.2);
    }
  }

}
</style>
