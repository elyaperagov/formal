<template>
  <section id="company" class="company">
    <h3 class="company__background-title">
      <p>Formal</p>
      <p>Crypto</p>
    </h3>

    <div class="company__blobs">
      <div v-if="!$root.isMobile" class="company__blob">
        <svg
          width="419"
          height="419"
          viewBox="0 0 419 419"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g filter="url(#filter0_f_1_1593)">
            <circle cx="209.5" cy="209.5" r="81.5" fill="#00FFC5" />
          </g>
          <defs>
            <filter
              id="filter0_f_1_1593"
              x="0"
              y="0"
              width="419"
              height="419"
              filterUnits="userSpaceOnUse"
              color-interpolation-filters="sRGB"
            >
              <feFlood flood-opacity="0" result="BackgroundImageFix" />
              <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
              <feGaussianBlur stdDeviation="50" result="effect1_foregroundBlur_1_1593" />
            </filter>
          </defs>
        </svg>
      </div>

      <div v-else class="company__blob">
        <svg
          width="148"
          height="148"
          viewBox="0 0 148 148"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g filter="url(#filter0_f_9_14)">
            <circle cx="74" cy="74" r="27" fill="#00FFC5" />
          </g>
          <defs>
            <filter
              id="filter0_f_9_14"
              x="0"
              y="0"
              width="148"
              height="148"
              filterUnits="userSpaceOnUse"
              color-interpolation-filters="sRGB"
            >
              <feFlood flood-opacity="0" result="BackgroundImageFix" />
              <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
              <feGaussianBlur stdDeviation="18" result="effect1_foregroundBlur_9_14" />
            </filter>
          </defs>
        </svg>
      </div>
    </div>

    <div class="container">
      <h2 tabindex="5">Company</h2>
      <div class="company__texts">
        <p>
          Formal Crypto – company-developer of&nbsp;digital products in the field of blockchain
          technologies
        </p>
        <p>
          We have been involved in a wide variety of&nbsp;projects, including the creation of DAOs,
          NFT collections, staking contracts, audits.
        </p>

        <p>
          Having extensive experience working with a&nbsp;variety of customers, we can join your
          project at any stage: from protocol design to&nbsp;turnkey development.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Company',
  methods: {}
}
</script>

<style lang="scss" scoped>
$i: 1;
$a: #{($i + 1) * 90};
$b: #{($i + 1) * 90+360};

svg:nth-child(#{$i}) {
  animation: move#{$i} #{($i) + 14}s infinite linear;
  cursor: grab;
}

@keyframes move#{$i} {
  from {
    transform: rotate(#{$a}deg) translate(#{(($i + 1)) * 75}px, 0.1px) rotate(-#{$a}deg);
  }
  to {
    transform: rotate(#{$b}deg) translate(#{(($i + 1)) * 75}px, 0.1px) rotate(-#{$b}deg);
  }
}
@media (max-width: 767px) {
  @keyframes move#{$i} {
    from {
      transform: rotate(#{$a}deg) translate(#{(($i + 1)) * 25}px, 0.1px) rotate(-#{$a}deg);
    }
    to {
      transform: rotate(#{$b}deg) translate(#{(($i + 1)) * 25}px, 0.1px) rotate(-#{$b}deg);
    }
  }
}
</style>
