<template>
  <div class="privacy-police">
    <div class="container privacy-police__wrap">
      <div class="privacy-police__header">
        <h1 class="base-title">Privacy policy</h1>
      </div>
      <div class="privacy-police__content">
        <button class="privacy-police__btn"><download-icon /> Donwload privacy_policy.pdf</button>
        <div
          class="privacy-police__content-item"
          v-for="(item, index) in $t('content')"
          :key="index"
        >
          <p class="privacy-police__content-title">{{ item.title }}</p>
          <p
            v-for="(p, i) in item.text"
            :key="i"
            class="privacy-police__content-text"
            v-html="p"
          >
          </p>
        </div>
      </div>
    </div>
    <div class="privacy-police__bg"></div>
  </div>
</template>

<i18n>
{
  "en": {
    "content": [
      {
        "title": "Our Commitment to Privacy",
        "text": ["Your privacy is very important to us. Part of our operation of this website involves the collection and use of information about you. This privacy policy explains what type of information we collect and what we do with that information to allow you to make choices about the way your information is collected and used."]
      },
      {
        "title": "What Information Do We Collect?",
        "text": ["In general, you can visit this website without identifying who you are or revealing any information about yourself. Information collected online can generally be categorized as anonymous or personally identifiable. Anonymous information is information that cannot be connected to the identity of a specific individual. Personally, identifiable information is information that specifically identifies a particular user, such as name, address, or phone number. An example of anonymous information is the fact that, while this website may record the number of visits to a particular page that occur in a given period of time, it does not necessarily tell us the names or other identifying information of every visitor. Many users of this website will choose not to provide any personally identifiable information; therefore, those individuals are anonymous to us, and any data collected about their use of this website is anonymous information."]
      },
      {
        "title": "Automatic Anonymous Information",
        "text": ["When you visit our site, we collect certain technical and routing information about your computer. For example, we log environmental variables such as browser type, operating system and CPU speed, and the Internet Protocol (IP) address of your originating Internet Service Provider, to try to bring you the best possible service. We also record search requests and results to try to ensure the accuracy and efficiency of our search engine. We use your IP address to track your use of the site, including pages visited and the time spent on each page. We collect this information and use it to measure the use of this website and to improve its content and performance. All of the information that is automatically submitted to us by your browser is considered anonymous information. To the extent we share such information with third parties, it is not traceable to any particular user and will not be used to contact you."]
      },
      {
        "title": "How Do We Use Information We Collect?",
        "text": ["We collect personally identifiable information only for providing the services you request, generating statistical studies, conducting marketing research, improving products and services, sending you surveys, and notifying you of new products and any other changes to our site or services that may affect you. When you submit personally identifiable information to us, you understand that you are agreeing to allow us to access, store, and use that information for those purposes.",
                "We will not sell or give any personally identifiable information to any third parties.",
                "We may be required by law enforcement or judicial authorities to provide personally identifiable information to the appropriate governmental authorities. If requested by law enforcement or judicial authorities, we will provide this information on receipt of the appropriate documentation. We may also release information to law enforcement agencies or other third parties if we feel it is necessary to protect the safety and welfare of our personnel or to enforce our terms of use."
        ]
      },
      {
        "title": "Opt-Out Policy",
        "text": ["If at any time you do not wish to receive offers and emails from us, we ask that you tell us. You may remove your name from our mailing list by sending us an email addressed to <b>questions@vendeta.network</b> and indicating in the subject line “No Offers or Email.” Or simply click the Unsubscribe button that is available in our every marketing campaign emails"]
      },
      {
        "title": "Security",
        "text": ["We operate secure data networks protected by industry standard firewall and password protection systems. Our security and privacy policies are periodically reviewed and enhanced as necessary, and only authorized individuals have access to the personally identifiable information provided by our users. We do not, however, guarantee that unauthorized, inadvertent disclosure will never occur."]
      },
      {
        "title": "Cookies",
        "text": ["This site uses cookies. Cookies are small data files, typically made up of a string of text and numbers, that assign you a unique identifier. This information enables your computer to have a “dialogue” with our site and permits us to administer our site more efficiently and to provide a more tailored and user-friendly service to you. You may set your browser to notify you when you receive a cookie or to prevent cookies from being sent; if you do so, this may limit the functionality we can provide you when you visit our site.",
                  "Third parties that link on this site may use cookies or collect other information when you go to their site. We do not control the collection or use of your information by these companies. You should contact these companies directly if you have any questions about their collection or use of information about you."
        ]
      }
    ]
  },
  "ch": {
  },
  "tur": {
  }
}
</i18n>

<style lang="scss" scoped>
.container {
  max-width: 950px;
}

.privacy-police {
  position: relative;
  z-index: 1;
  min-height: 100vh;

  &::before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    width: 1445px;
    height: 749px;
    background-image: url('../assets/img/map.svg');
    background-position: center;
    background-repeat: no-repeat;
    z-index: -1;
    pointer-events: none;
    background-size: contain;

    @media (max-width: 767px) {
      width: 1128px;
      height: 591px;
      left: -137px;
      top: -5px;
    }
  }

  &::after {
    content: '';
    position: absolute;
    right: -230.14px;
    top: 85px;
    width: 2452.13px;
    height: 1583.98px;
    mix-blend-mode: normal;
    filter: blur(150px);
    transform: rotate(-9.91deg);
    background: linear-gradient(
      89.98deg,
      rgba(152, 207, 225, 0) 5.81%,
      #98cfe1 98.35%
    );
    z-index: -2;
    pointer-events: none;
  }

  &__wrap {
    padding-top: 175px;
    padding-bottom: 80px;

    @media(max-width: 767px) {
      padding-top: 100px;
    }
  }

  &__content {
    width: 100%;
    padding: 64px 87px 36px;
    background: #ffffff;
    border-radius: 36px;
    max-width: 950px;
    margin: 0 auto;
    position: relative;
    z-index: 2;

    @media(max-width: 767px) {
      padding: 47px 26px;
    }
  }

  &__content-item {
    &:not(:last-child) {
      margin-bottom: 60px;


      @media(max-width: 767px) {
        margin-bottom: 55px;
      }
    }
  }

  &__content-title {
    font-size: 28px;
    line-height: 40px;
    color: #00b4db;
    margin-top: 0;
    margin-bottom: 30px;

    @media(max-width: 767px) {
      font-size: 24px;
      line-height: 35px;
    }
  }

  &__content-text {
    font-size: 18px;
    line-height: 26px;
    color: rgba(51, 51, 51, 0.8);
    max-width: 690px;

    &:not(:last-child) {
      margin-bottom: 35px;
    }

    @media(max-width: 767px) {
      font-size: 16px;
      line-height: 23px;

      &:not(:last-child) {
        margin-bottom: 25px;
      }
    }
  }

  &__bg {
    position: relative;
    z-index: 1;

    &::before {
      content: '';
      position: absolute;
      bottom: -798.95px;
      left: -850px;
      width: 2452.14px;
      height: 1583.98px;
      background: linear-gradient(
          89.98deg,
          rgba(152, 207, 225, 0) 5.81%,
          #98cfe1 98.35%
      );
      mix-blend-mode: normal;
      filter: blur(150px);
      transform: matrix(-0.99, -0.17, -0.17, 0.99, 0, 0);
      z-index: -1;
      pointer-events: none;
    }
  }

  &__btn {
    font-size: 16px;
    line-height: 23px;
    color: #576280;
    border: none;
    outline: none;
    background: transparent;
    cursor: pointer;
    display: flex;
    align-items: center;
    margin-bottom: 20px;

    svg {
      margin-right: 10px;
    }
  }
}
</style>
<script>
import DownloadIcon from "@/components/icon/DownloadIcon";
export default {
  components: {DownloadIcon}
}
</script>
