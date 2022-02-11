<template>
  <Layout>
    编辑标签
  </Layout>
</template>

<script lang="ts">
import Vue from 'vue';
import {Component} from 'vue-property-decorator';


@Component
export default class EditLabel extends Vue{
  created(){
    console.log(this.$route.params);
  }
}
</script>

<style lang="scss" scoped>

</style>