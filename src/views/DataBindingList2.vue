<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>제품명</th>
          <th>가격</th>
          <th>카테고리</th>
          <th>배송료</th>
        </tr>
      </thead>
      <tbody>
        <tr :key="i" v-for="(product, i) in productList">
          <td>{{ product.product_name }}</td>
          <td>{{ product.price }}</td>
          <td>{{ product.category }}</td>
          <td>{{ product.delivery_price }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
/* eslint-disable */
/* input에 텍스트를 입력하는 순간 버튼이 활성화
    v-model=textValue가 비어있는 경우는 버튼이 비활성화 */
export default {
  name: "databindinglist2",
  data() {
    return {
      productList: [],
    };
  },
  created() {
    this.getList();
  },
  methods: {
    async getList() {
      this.productList = await this.$api(
        "https://d7f6b647-4294-4462-9b34-49bbaea88a97.mock.pstmn.io/list",
        "get"
      );
    },
  },
};
</script>

<style scope>
table {
  border-collapse: collapse;
  width: 100%;
}
td,
th {
  border: 1px solid #dddddd;
  text-align: center;
  padding: 8px;
}
</style>
