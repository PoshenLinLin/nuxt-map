<template>
    <div class="info__card">

    </div>
</template>

<script>
    export default{
        components:{},
        prop: {
          item: {
            type: Object,
            default: {}
          }
        },
        data:() => ({
          defaultItem: {

          }
        }),
        methods:{
          init() {
          }
        },
        mounted(){}
    }
</script>

<style lang="css" scoped>
.info__card{
  width: 100%;
  background-color: #35495e;
}
</style>
