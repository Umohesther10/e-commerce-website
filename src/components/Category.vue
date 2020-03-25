<template>
  <div class="cate">
    <ul>
      <li class="change">
        <b-row>
          <b-col cols="1">
            <i :class="category.icon"></i>
          </b-col>

          <b-col>{{ category.name }}</b-col>
        </b-row>
      </li>
    </ul>

    <!-- <b-list-group style=" margin-top: 5px;">
      <b-list-group-item button>{{ category.name }}</b-list-group-item>
    </b-list-group>-->
  </div>
</template>

<script>
export default {
  name: "Category",
  props: ["category"]
};
</script>
<style scoped>
.change {
  list-style-type: none;
  font-size: 15px;
}
.change:hover {
  color:#0373fc;
  cursor: pointer;
}
</style>
