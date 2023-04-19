<script setup lang="ts">
import {reactive, provide} from "vue";
import BaseSection from "./components/BaseSection.vue";
import type {Member} from "./interfaces";

// 会員情報リストの用意
const memberList = new Map<number, Member>();
memberList.set(33456, {id: 33456, name: "田中太郎", email: "bow@example.com", points: 35, note: "初回入会特典あり"});
memberList.set(47783, {id: 47783, name: "鈴木次郎", email: "mue@example.com", points: 53});

// 会員情報をProvide
provide("memberList", reactive(memberList));
</script>

<template>
  <BaseSection />
</template>

<!-- <style>
section {
  border: blue 1px solid;
  margin: 10px;
}
</style> -->