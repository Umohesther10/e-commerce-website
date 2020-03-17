<template>
  <div>
    <b-list-group style=" margin-top: 5px;">
      <b-list-group-item button>{{ category.name }}</b-list-group-item>
    </b-list-group>
  </div>
</template>

<script>
export default {
  name: "Category",
  props: ["category"]
};
</script>

