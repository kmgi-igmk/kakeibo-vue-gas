<template>
  <div class="container">
    <div class="alert alert-success" id="success-msg"></div>
    <div class="alert alert-danger" id="err-msg"></div>
    <header>
      <h1>{{ title }}</h1>
      <div class="row m-2 row-cols-auto">
        <div class="col-md-auto px-0">
          <select class="form-select" id="yearOfSheet"></select>
        </div>
        <div class="col px-0 align-self-center">年のスプレッドシートに登録</div>
      </div>
    </header>
    <main>
      <!-- 1件分のデータ入力部分 -->
      <div class="container-sm pt-2 pb-2 bg-info rounded">
        <form id="onerecord" class="row gy-2 gx-3">
          <div class="col-auto">
            <div class="form-floating">
              <select id="inputType" class="form-select inputs" aria-label="type" required></select>
              <label for="inputType" class="form-label">項目</label>
            </div>
          </div>
          <div class="col-auto">
            <div class="form-floating">
              <input type="number" class="form-control inputs" id="inputPrice" placeholder="1" value="1000" required>
              <label for="inputPrice" class="form-label">金額</label>
            </div>
          </div>
          <div class="col-auto">
            <div class="form-floating">
              <input type="text" class="form-control inputs" id="inputStore" required>
              <label for="inputStore" class="form-label">店名</label>
            </div>
          </div>
          <div class="col-auto">
            <div class="form-floating">
              <select id="inputMonth" class="form-select inputs" aria-label="month" required></select>
              <label for="inputMonth" class="form-label">〆月</label>
            </div>
          </div>
          <div class="col-auto">
            <div class="form-floating">
              <select id="inputPayer" class="form-select inputs" aria-label="payer" required>
                <option value="健太" selected>健太</option>
                <option value="明子">明子</option>
              </select>
              <label for="inputPayer" class="form-label">支払った人</label>
            </div>
          </div>
          <div class="col-auto">
            <div class="form-floating">
              <input type="text" class="form-control inputs" id="inputRemarks">
              <label for="inputRemarks" class="form-label">備考</label>
            </div>
          </div>
          <div class="col-auto">
            <button type="button" class="btn mt-1 btn-primary btn-lg" id="addBtn">追加</button>
          </div>
        </form>
      </div>
      <!-- 複数件分のデータ保持部分 -->
      <div class="container-sm mt-2">
        <table id="registerData" class="table table-striped table-hover">
          <thead id="thead">
            <tr></tr>
          </thead>
          <tbody id="tbody">
          </tbody>
        </table>
      </div>      
      <div class="container-sm">
        <div class="d-flex justify-content-center">
          <button type="button" id="registerBtn" class="btn btn-danger w-50 btn-lg">登録</button> 
        </div>
      </div>
    </main>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Register",
  props: {
    title: String,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
