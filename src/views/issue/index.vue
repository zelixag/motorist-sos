<template>
  <div class="page-issue h-[calc(100vh-156px)]">
    <div class="bg-[#fff] h-[68px] flex items-center">
      <div class="ml-[40px] text-[24px]">Whats the issue</div>
    </div>
    <div class="mb-[40px] mx-[24px]">
      <div class="text-[18px] text-center mt-[60px]">Take a quick quiz</div>
      <div class="mt-[32px]">
        Welcome to the MotoristSOS diagnosing quiz. Let’s find the problem
        together with this 2 minute questionnaire, made by real mechanics. Enter
        your details below:
      </div>
    </div>

    <van-cell-group inset>
      <van-field label="Year" label-class="label-customer" />
      <van-field label="Make" label-class="label-customer" />
      <van-field label="Model" label-class="label-customer" />
      <van-field
        label="Email Address"
        label-class="label-customer"
        label-width="100px"
      />
    </van-cell-group>
    <van-checkbox-group class="mx-[24px] mt-[32px] text-[10px]" shape="square">
      <van-checkbox name="a"
        >Receive results and updates about my diagnosis</van-checkbox
      >
    </van-checkbox-group>
    <div
      class="mt-[60px] mx-[24px]"
      @click="
        () => {
          router.push({ name: 'FlatBattery' });
        }
      "
    >
      <van-button
        round
        block
        type="primary"
        native-type="submit"
        color="#3A4855"
      >
        Start
      </van-button>
    </div>
  </div>
</template>

<script setup lang="ts" name="Issue">
import { useRouter } from "vue-router";
const router = useRouter();
</script>

<style>
.label-customer {
  color: #0073ba;
}
.page-issue {
  background: rgba(0, 115, 186, 0.03);
}
</style>
