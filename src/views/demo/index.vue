<script setup lang="ts" name="Demo">
import { reactive, ref } from "vue";
import { useRouter } from "vue-router";
const active = ref("battery");
const router = useRouter();
const gridList = [
  {
    iconName: "battery",
    title: "Flat Battery"
  },
  {
    iconName: "unsure",
    title: "Engine Smoke"
  },
  {
    iconName: "tow-truck",
    title: "Tow Truck"
  },
  {
    iconName: "flat-tyre",
    title: "Flat Tyre"
  },
  {
    iconName: "locked-out",
    title: "Locked Out"
  },
  {
    iconName: "out-of-fuel",
    title: "Out of Fuel"
  },
  {
    iconName: "oil-leak",
    title: "Oil Leak"
  },
  {
    iconName: "car-accident",
    title: "Car Accident"
  },
  {
    iconName: "unsure",
    title: "Unsure"
  }
];
</script>

<template>
  <div class="demo-content px-[12px]">
    <div class="bg-blue-500 h-[68px] flex items-center">
      <div class="ml-[40px] text-[24px] text-[#fff]">Back</div>
    </div>
    <div
      class="font-[700] text-[24px] flex justify-center text-center mt-[8px]"
    >
      Please select the problem you are currently facing.
    </div>
    <div class="mt-[32px] grid grid-cols-3 grid-rows-3 gap-x-[8px] gap-y-[8px]">
      <div
        v-for="item in gridList"
        :key="item.iconName"
        @click="
          () => {
            active = item.iconName;
            router.push({ name: 'Issue' });
          }
        "
        class="grid-item rounded-[20px] w-[110px] h-[110px] flex flex-col justify-center items-center"
        :class="`${
          active === item.iconName
            ? 'bg-[#57A1ED] border-[#FF8C00] border-[5px] text-[#fff]'
            : 'bg-[#e5e5e5] text-[#57A1ED]'
        }`"
      >
        <svg-icon :name="item.iconName" class="text-[60px]"></svg-icon>
        <div class="mt-16px">{{ item.title }}</div>
      </div>
    </div>
  </div>
</template>

<style>
.grid-item {
  box-shadow: 0px 2px 3px 0px rgba(0, 0, 0, 0.25);
}
</style>
