<script setup lang="ts">
import { NDataTable } from "naive-ui";

interface RowData {
  id: number;
  name: string;
}

const columns = [
  {
    key: "id",
    title: "ID",
  },
  {
    key: "name",
    title: "Name",
  },
];

const data: RowData[] = [];

for (let i = 0; i < 100; i++) {
  data.push({
    id: i + 1,
    name: `Name ${i}`,
  });
}
</script>

<template>
  <div>
    <NDataTable
      :columns="columns"
      :data="data"
      :max-height="500"
      virtual-scroll
    />
  </div>
</template>

<style scoped></style>
