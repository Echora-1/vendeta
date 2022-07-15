<template>
  <div class="container download-block">
    <div class="download-block__wrap">
      <div class="download-block__left">
        <h2 class="base-title">Download application</h2>
        <p class="base-subtitle">No matter where you are or what devices you’re using, VENDETA VPN has you connected and secure your online activity through a truly secure decentralised VPN just one tap away.</p>
      </div>
      <div class="download-block__right">
        <base-tabs>
          <base-tab v-for="(tab, index) in $t('platforms')" :key="index" :title="tab.title">
            <download-card :content="tab" />
          </base-tab>
        </base-tabs>
      </div>
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "platforms": [
      {
        "title": "Android",
        "img": "code"
      },
      {
        "title": "iOS",
        "img": "code"
      },
      {
        "title": "Windows",
        "img": "code"
      }
    ]
  },
  "ch": {
    "platforms": [
      {
        "title": "Android",
        "img": "code"
      },
      {
        "title": "iOS",
        "img": "code"
      },
      {
        "title": "Windows",
        "img": "code"
      }
    ]
  },
  "tur": {
    "platforms": [
      {
        "title": "Android",
        "img": "code"
      },
      {
        "title": "iOS",
        "img": "code"
      },
      {
        "title": "Windows",
        "img": "code"
      }
    ]
  }
}
</i18n>

<script>
import BaseTabs from "@/components/base/BaseTabs";
import BaseTab from "@/components/base/BaseTab";
import DownloadCard from "@/components/main/DownloadCard";
export default {
  components: {DownloadCard, BaseTab, BaseTabs}
}
</script>

<style lang="scss" scoped>

.base-title {
  margin-bottom: 16px;
}

.base-subtitle {
  max-width: 394px;
}

.download-block {
  &__wrap {
    background: #FFFFFF;
    border-radius: 36px;
    padding: 90px 74px;
    display: flex;
  }


  &__right {
    flex: 0 0 52%;
    max-width: 52%;
  }

  &__left {
    flex: 0 0 48%;
    max-width: 48%;
    padding-right: 16px;
    padding-top: 20px;
  }

}
</style>
