<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>제품명</th>
          <th>가격</th>
          <th>카테고리</th>
        </tr>
      </thead>
      <tbody>
        <tr :key="i" v-for="(product, i) in productList">
          <td>{{ product.product_name }}</td>
          <td>{{ product.product_price }}</td>
          <td>{{ product.product_category }}</td>
        </tr>
      </tbody>
    </table>

    <br />

    <select name="" id="" v-model="selectedValue" @change="changeSelect">
      <option value="서울">서울</option>
      <option value="부산">부산</option>
      <option value="제주">제주</option>
    </select>
  </div>
</template>

<script>
/* eslint-disable */
/* input에 텍스트를 입력하는 순간 버튼이 활성화
    v-model=textValue가 비어있는 경우는 버튼이 비활성화 */
export default {
  name: "databindinglist",
  data() {
    return {
      productList: [
        {
          product_name: "기계식 키보드",
          product_price: "30000",
          product_category: "노트북/태블릿",
        },
        {
          product_name: "무선마우스",
          product_price: "10000",
          product_category: "노트북/태블릿",
        },
        {
          product_name: "무선충전기",
          product_price: "40000",
          product_category: "노트북/태블릿",
        },
      ],
      selectedValue: "",
    };
  },
  methods: {
    changeSelect() {
      alert(this.selectedValue);
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
