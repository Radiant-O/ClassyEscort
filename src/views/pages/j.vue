<template>
  <body class="overflow-hidden mb-6">
    <div class="lg:w-[70%] mx-auto mt-5">
      <p class="text-2xl items-center">
        <ArrowLeftOutlined @click="$router.back()"/>
      </p>
    </div>
    <div
      class="md:flex items-start justify-center py-12 2xl:px-20 md:px-6 px-4"
    >
      <div class="md:w-[35%]">
        <a-carousel arrows>
          <template #prevArrow>
            <div class="custom-slick-arrow" style="left: 10px; z-index: 1">
              <left-circle-outlined />
            </div>
          </template>
          <template #nextArrow>
            <div class="custom-slick-arrow" style="right: 10px">
              <right-circle-outlined />
            </div>
          </template>
          <div>
            <img
              class="w-[100%]"
              alt="ashylnn"
              src="../../assets/images/sindee.jpeg"
            />
          </div>
          <div>
            <img
              class="w-[100%]"
              alt="ashylnn"
              src="../../assets/images/sindee1.jpeg"
            />
          </div>
        </a-carousel>
      </div>

      <div class="xl:w-2/5 md:w-1/2 lg:ml-8 md:ml-6 md:mt-0 mt-6">
        <div>
          <h1
            class="lg:text-2xl text-xl font-semibold text-gray-800 mt-2"
          >
            Sindee
          </h1>
        </div>
        <div
          class="pt-1 border-b border-gray-200 flex items-center justify-between"
        >
          <div class="flex items-center justify-center">
            <p class="text-sm leading-none text-gray-600">
              25
            </p>
          </div>
        </div>
        <div
          class="py-4 border-b border-gray-200 flex items-center justify-between"
        >
          <p class="text-base leading-4 text-gray-800">
            Missouri
          </p>
        </div>
        <button
          class="focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-800 text-base flex items-center justify-center leading-none text-white bg-gray-800 w-full py-4 hover:bg-gray-700"
        >
        <a class="flex items-center gap-1" href="https://t.snapchat.com/Hp9WUVFn"
        ><img class="w-[30px]" src="../../assets/icons/s1.png" />
          I'm Interested</a
      >
        </button>
        <div>
          <p class="mt-7 text-lg font-medium">Reviews:</p>
          <p
            class="text-base lg:leading-tight leading-normal italic text-gray-600"
          >
          I'm lucky to know her; she adds a touch of magic to every interaction. Her presence is like a breath of fresh air, filling my world with warmth and happiness. Her infectious laughter and radiant smile have a way of making any day brighter, and her kindness is simply unparalleled. She's a remarkable person, and I treasure the moments we share.
          </p>
        </div>
        <div>
          <div class="border-t border-b py-4 mt-7 border-gray-200">
            <div
              @click="showList"
              data-menu
              class="flex justify-between items-center cursor-pointer"
            >
              <p class="text-base leading-4 text-gray-800">
                Prices / Rates:
              </p>
              <button
                class="cursor-pointer focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-400 rounded"
                role="button"
                aria-label="show or hide"
              >
                <img
                  v-if="showData == false"
                  class="transform"
                  src="https://tuk-cdn.s3.amazonaws.com/can-uploader/productDetail3-svg4.svg"
                  alt="dropdown"
                />
                <img
                  v-if="showData == true"
                  class="transform rotate-180"
                  src="https://tuk-cdn.s3.amazonaws.com/can-uploader/productDetail3-svg4.svg"
                  alt="dropdown"
                />
              </button>
            </div>
            <div
              v-if="showData"
              class="text-base leading-normal pr-12 mt-4 text-gray-600"
              id="sect"
            >
              <p
                class="text-base leading-4 mt-7 text-gray-600"
              >
                1hour - $200
              </p>
              <p
                class="text-base leading-4 mt-4 text-gray-600"
              >
                2hour - $400
              </p>
              <p
                class="text-base leading-4 mt-4 text-gray-600"
              >
                3hour - $600
              </p>
              <p
                class="text-base leading-4 mt-4 text-gray-600"
              >
                6hour - $1000
              </p>
              <p
                class="text-base leading-4 mt-4 text-gray-600"
              >
                Weekend - $2000
              </p>
            </div>
          </div>
        </div>
        <div>
          <div class="border-b py-4 border-gray-200">
            <div
              @click="showList1"
              data-menu
              class="flex justify-between items-center cursor-pointer"
            >
              <p class="text-base leading-4 text-gray-800">
                About
              </p>
              <button
                class="cursor-pointer focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-400 rounded"
                role="button"
                aria-label="show or hide"
              >
                <img
                  v-if="showData1 == false"
                  class="transform"
                  src="https://tuk-cdn.s3.amazonaws.com/can-uploader/productDetail3-svg4.svg"
                  alt="dropdown"
                />
                <img
                  v-if="showData1 == true"
                  class="transform rotate-180"
                  src="https://tuk-cdn.s3.amazonaws.com/can-uploader/productDetail3-svg4.svg"
                  alt="dropdown"
                />
              </button>
            </div>
            <div
              v-if="showData1"
              class="text-base leading-normal pr-12 mt-4 text-gray-600"
              id="sect"
            >
              Thank you for clicking on my profile I hope you like it. I love to meet new people . I
              am open to date individuals and I am straight , 🥵🥵so far I am 100% natural I
              don't have any surgery . Will always be very pleased 🌪️🔥
            </div>
          </div>
        </div>
        <button
          class="focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-800 text-base flex items-center justify-center leading-none text-white bg-gray-800 w-full py-4 hover:bg-gray-700"
        >
        <a class="flex items-center gap-1" href="https://wa.me/message/3RXA5RDT6CKDP1"
        ><img class="w-[25px]" src="../../assets/icons/w1.png" />
        Contact Sindee</a
      >
        </button>
      </div>
    </div>
  </body>
</template>

<script setup>
import { ref } from "vue";
import { LeftCircleOutlined, RightCircleOutlined, ArrowLeftOutlined } from "@ant-design/icons-vue";

const showData = ref(false);
const showData1 = ref(false);

const showList = () => {
  showData.value = !showData.value;
};

const showList1 = () => {
  showData1.value = !showData1.value;
};
</script>

<style scoped>
:deep(.slick-slide) {
  text-align: center;
  height: 35rem;
  line-height: 160px;
  overflow: hidden;
}

:deep(.slick-arrow.custom-slick-arrow) {
  width: 25px;
  height: 25px;
  font-size: 25px;
  color: rgb(4, 7, 11);
  transition: ease all 0.3s;
  opacity: 0.3;
  z-index: 1;
}
:deep(.slick-arrow.custom-slick-arrow:before) {
  display: none;
}
:deep(.slick-arrow.custom-slick-arrow:hover) {
  color: #fff;
  opacity: 0.5;
}

:deep(.slick-slide h3) {
  color: #fff;
}
</style>
