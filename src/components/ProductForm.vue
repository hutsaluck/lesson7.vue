<script>
import {defineComponent, ref, onMounted} from "vue";
import Loader from "@/components/Loader.vue";
import {useProductStore} from "@/store/index.js";

export default defineComponent({
  name: "ProductForm",
  components: {Loader},
  emits: ['product-added'],
  setup(_,{emit}){
    const title = ref('')
    const price = ref('')

    const handleSubmit = () => {
      emit("product-added", {title: title.value, price: Number(price.value), id: "@"})
      title.value = ''
      price.value = ''
    }

    return{
      title,
      price,
      handleSubmit,
    }
  }
})
</script>

<template>
  <form @submit.prevent="handleSubmit">
    <p>Create product</p>
    <div class="inputs-container">
      <div class="title-block">
        <label for="title">Title</label>
        <input type="text" id="title" v-model="title">
      </div>
      <div class="price-block">
        <label for="price">Price</label>
        <input type="number" id="price" v-model="price">
      </div>

      <input type="submit" value="Add Product" />
    </div>
  </form>
</template>

<style scoped>

</style>
