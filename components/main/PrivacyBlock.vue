<template>
  <div class="container privacy-block">
    <div class="privacy-block__left">
      <h2 class="base-title">{{ $t('title') }}</h2>
      <p class="base-subtitle">{{ $t('subtitle') }}</p>
      <ul>
        <li v-for="(li, index) in $t('list')" :key="index" class="base-list-item">
          <span>
            {{ li }}
          </span>
        </li>
      </ul>
    </div>
    <div class="privacy-block__right">
      <img class="privacy-block__image" src="../../assets/img/privacy.png" alt="privacy" width="434" height="427">
    </div>
  </div>
</template>


<i18n>
{
  "en": {
    "title": "Privacy is priority",
    "subtitle": "Based on a decentralized structure, VENDETA empowers you to regain your internet privacy and stay invisible from all kinds of surveillance and censorship.",
    "list": ["Our network lasts foreverand enables you to bypass firewalls and geo-restrictions.", "Decentralized community is powered by individuals like you, data is generated and distributed amongst users.", "We built a decentralized network so single points of attack or failure pose no risk at all."]
  },
  "ch": {
    "title": "Privacy is priority",
    "subtitle": "Based on a decentralized structure, VENDETA empowers you to regain your internet privacy and stay invisible from all kinds of surveillance and censorship.",
    "list": ["Our network lasts foreverand enables you to bypass firewalls and geo-restrictions.", "Decentralized community is powered by individuals like you, data is generated and distributed amongst users.", "We built a decentralized network so single points of attack or failure pose no risk at all."]
  },
  "tur": {
    "title": "Privacy is priority",
    "subtitle": "Based on a decentralized structure, VENDETA empowers you to regain your internet privacy and stay invisible from all kinds of surveillance and censorship.",
    "list": ["Our network lasts foreverand enables you to bypass firewalls and geo-restrictions.", "Decentralized community is powered by individuals like you, data is generated and distributed amongst users.", "We built a decentralized network so single points of attack or failure pose no risk at all."]
  }
}
</i18n>

<style lang="scss" scoped>

.base-title {
  margin-top: 0;
  margin-bottom: 10px;
}

.base-subtitle {
  max-width: 575px;
  margin-bottom: 36px;
}

.base-list-item {
  max-width: 470px;
}

.privacy-block {
  display: flex;

  @media(max-width: 767px) {
    flex-direction: column;
    max-width: 425px;
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
    }
  }

  &__image {
    object-fit: contain;
    position: relative;
    left: 35px;
    top: 12px;
    width: 100%;
    height: 100%;
    max-width: 434px;
    max-height: 427px;

    @media(max-width: 1000px) {
      left: 0;
    }
  }
}
</style>
