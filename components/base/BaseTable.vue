<template>
  <table>
    <thead>
    <tr>
      <th v-for="(item, index) in data.th" :key="index">{{ item }}</th>
    </tr>
    </thead>
    <tbody>
    <tr v-for="(items, index) in data.td" :key="index">
      <td v-for="(item, i) in items" :key="i">{{item}}</td>
    </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      default: () => {
        return {
          th: [],
          td: []
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
table {
  border-collapse: collapse;
  width: 100%;
}

tr {
  &:not(:last-child) {
    border-bottom: 1px solid #57628033;
  }

  &:first-child {
    border-bottom: 2px solid #57628033;
  }
}

td, th {
  text-align: left;

  &:last-child {
    text-align: right;
  }
}


th {
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #576280;
  opacity: 0.4;
  padding: 0 0 13px;
}

td {
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #576280;
  padding: 16px 0;
}

</style>
