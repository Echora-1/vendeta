<template>
  <div class="choice-table">
    <div class="choice-table__item">
      <div class="choice-table__sub-item"></div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/logo/vendeta.svg"
          width="130"
          height="35"
          alt=""
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/logo/purevpn.png"
          width="130"
          height="35"
          alt=""
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/logo/nordvpn.png"
          width="130"
          height="35"
          alt=""
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/logo/privatevpn.png"
          width="130"
          height="35"
          alt=""
        />
      </div>
    </div>
    <div class="choice-table__item">
      <div class="choice-table__sub-item">
        <span> Price </span>
      </div>
      <div class="choice-table__sub-item">
        <span>
          35.00 USDT<br />
          (for 2 year)</span
        >
      </div>
      <div class="choice-table__sub-item">
        <span> 47.76 USDT<br /> (mo/ from 2 year) </span>
      </div>
      <div class="choice-table__sub-item">
        <span> 63.48 USDT<br /> (mo/ from 2 year) </span>
      </div>
      <div class="choice-table__sub-item">
        <span> 72.00 USDT<br /> (mo/ for 1 year) </span>
      </div>
    </div>
    <div class="choice-table__item">
      <div class="choice-table__sub-item">
        <span>24/7 support</span>
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
    </div>
    <div class="choice-table__item">
      <div class="choice-table__sub-item">
        <span>Ad blocker</span>
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
    </div>
    <div class="choice-table__item">
      <div class="choice-table__sub-item">
        <span>Two-factor authentication</span>
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
    </div>
    <div class="choice-table__item">
      <div class="choice-table__sub-item">
        <span>Dedicated channel</span>
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
    </div>
    <div class="choice-table__item">
      <div class="choice-table__sub-item">
        <span>Decentralized <br /> & Secured</span>
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-on.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
      <div class="choice-table__sub-item">
        <img
          src="../../assets/img/check-off.png"
          alt="check"
          width="20"
          height="20"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.choice-table {
  background: transparent;
  width: 100%;
  display: flex;

  &__item {
    width: calc(1240px / 7);

    &:nth-child(even) {
      background: linear-gradient(
        180deg,
        #ffffff 0%,
        rgba(255, 255, 255, 0) 100%
      );
      border-radius: 12px;
    }

    &:first-child {
      & > div:nth-child(2) {
        border-radius: 12px 0 0 12px;
      }
    }

    &:last-child {
      & > div:nth-child(2) {
        border-radius: 0 12px 12px 0;
      }
    }
  }

  &__sub-item {
    min-height: calc(452px / 5);
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;

    &:nth-child(2) {
      background: #ffffff;
      box-shadow: 0 8px 32px -12px rgba(0, 180, 219, 0.16);
    }

    span {
      font-size: 18px;
      line-height: 26px;
      text-align: center;
      color: #333333;
      opacity: 0.7;
      max-width: 140px;
    }

    img {
      object-fit: contain;
    }

    &:first-child {
      span {
        font-weight: 500;
      }
    }
  }
}
</style>
