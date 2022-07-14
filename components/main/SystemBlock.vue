<template>
  <div class="container system-block">
    <div class="system-block__left">
      <img src="../../assets/img/system.svg" alt="system" />
    </div>
    <div class="system-block__right">
      <h2 class="base-title">{{ $t('title') }}</h2>
      <p class="base-subtitle">
        {{ $t('subtitle')[0] }}<br /><br />
        {{ $t('subtitle')[1] }}
      </p>
      <ul>
        <li v-for="(li, index) in $t('list')" :key="index" class="system-block__list-item">
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

  &__left,
  &__right {
    flex: 0 0 50%;
    max-width: 50%;
  }

  &__left {
    padding-right: 16px;
  }

  &__right {
    padding-left: 16px;
    padding-top: 25px;
  }

  &__list-item {
    font-size: 18px;
    line-height: 28px;
    color: #333333;
    position: relative;
    padding-left: 16px;

    &:not(:last-child) {
      margin-bottom: 22px;
    }

    &:before {
      content: '';
      position: absolute;
      width: 6px;
      height: 6px;
      background: #00b4db;
      top: 11px;
      left: 0;
      transform: rotate(45deg);
    }
  }
}
</style>
