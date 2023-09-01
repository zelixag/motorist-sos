<template>
  <div
    class="page-flat-battery h-[calc(100vh-236px)] flex items-center flex-col relative"
  >
    <div class="bg-[#fff] h-[68px] flex items-center">
      <div class="ml-[40px] text-[24px]">Flat Battery</div>
    </div>
    <div class="relative">
      <van-image width="327" height="218" radius="20px" :src="imgPng" />
      <div
        class="bg-[#0073BA] absolute bottom-[6px] px-[12px] text-[#fff] left-0 rounded-[5px 5px 0px 20px;]"
      >
        How to check a flat battery
      </div>
    </div>
    <div class="relative">
      <van-image width="327" height="218" radius="20px" :src="imgPng" />
      <div
        class="bg-[#0073BA] absolute bottom-[6px] px-[12px] text-[#fff] left-0 rounded-[5px 5px 0px 20px;]"
      >
        How to check a flat battery
      </div>
    </div>
    <div class="mt-[24px] w-[80%] mx-[32px]">
      <van-button round block color="#C4C4C4">Find a mechanic</van-button>
    </div>
    <div class="mt-[24px] w-[80%] mx-[32px]">
      <van-button class="mt-[16px]" round block>Problem resolved</van-button>
    </div>

    <div
      class="mt-[60px] mx-[24px] w-full absolute bottom-[-227px]"
      @click="handleClick"
    >
      <div
        class="bg-[#3A4855] text-[24px] text-[#fff] rounded-[40px] h-[154px] flex justify-center pt-[16px]"
        size="large"
      >
        Your checklist
      </div>
    </div>
  </div>
  <van-action-sheet
    v-model:show="showBottom"
    :overlay="false"
    title="Your checklist"
    close-on-click-action
  >
    <div class="content h-[400px] bg-[#3A4855] text-[#fff]">
      Power soruce (jump battery or another car)Power soruce (jump battery or
      another car)Power soruce (jump battery or another car)Power soruce (jump
      battery or another car)Power soruce (jump battery or another car)
    </div>
  </van-action-sheet>
</template>

<script setup lang="ts" name="Flat-battery">
import { reactive, ref } from "vue";
import imgPng from "./images/flat-battery.png";
const showBottom = ref(false);
const handleClick = () => {
  showBottom.value = true;
};
</script>

<style>
.label-customer {
  color: #0073ba;
}
.page-issue {
  background: rgba(0, 115, 186, 0.03);
}
.van-action-sheet__header {
  background: #3a4855;
  color: #fff;
  font-size: 24px;
}
</style>
