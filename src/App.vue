<script>
import {defineComponent} from "vue";
import ProductList from "@/components/ProductList.vue";

export default defineComponent({
  name: "App",
  components: {ProductList},
  setup(){
    return{

    }
  }
})
</script>

<template>
  <ProductList />
</template>

<style>
*{
  font-family: 'Lexend', sans-serif;
}
ul{
  list-style-type: none;
  padding: 0;
}
button{
  cursor: pointer;
  border: 1px solid rgba(0, 0, 0, 0.3);
  padding: 5px 10px;
  font-style: normal;
  font-weight: 600;
  font-size: 19px;
  text-align: center;
  color: #fff;
  background-color: #79c56e;
  border-radius: 6px;
}
</style>
