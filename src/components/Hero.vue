<template>
  <div class="hero bg-primary">
    <br />
    <div class="myBox p-4 mt-4 mb-2">
      <br />
      <b-row style="width: 1390px">
        <b-card
          v-for="product in products"
          v-show="product.id < 4"
          :key="product.id"
          class="slidercard ml-4 mb-2"
          style="
            background-image: url(../assets/images/image-1.jpg);
            border-radius: 10px;
            width: 420px;
            height: 300px;
          "
        >
          <h3 href="#" class="card-title text-right">
            <b-icon-box-arrow-up-right></b-icon-box-arrow-up-right>
          </h3>
          <h3 class="text-bawah">
            {{ product.nama }} <br />
            <strong
              ><a href="#" class="card-link text-light">{{
                product.gambar
              }}</a></strong
            >
          </h3>
        </b-card>
      </b-row>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Hero",
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProducts(data) {
      this.products = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/best-products")
      .then((response) => this.setProducts(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
.b-form-group {
  border-radius: 10px;
}

.text-bawah {
  position: absolute;
  bottom: 20px;
  left: 25px;
  color: white;
}
</style>