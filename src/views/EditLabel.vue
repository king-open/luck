<template>
  <Layout>
    编辑标签
  </Layout>
</template>

<script lang="ts">
import Vue from 'vue';
import {Component} from 'vue-property-decorator';
import tagListModel from '@/models/tagListModel';

@Component
export default class EditLabel extends Vue{
  created(){
    const id = this.$route.params.id;
    console.log(id);
    tagListModel.fetch();
    console.log(tagListModel);
    const tags =tagListModel.data;
    console.log(tags);

    const tag = tags.filter(t => t.id === id)[0];
    console.log(tag);

    if(tag){
      console.log(tag);
    }else{
      this.$router.replace('/404');
    }
  }
}
</script>

<style lang="scss" scoped>

</style>