<template>

  <div class="card-product mb-2" style="max-width: 13rem;">
      <img class="card-product" src="../assets/images/image-1.jpg" width="100%">
     <p class="m-0"><p class="mt-2 bg">
          <strong><a href="#" class="card-link">{{ ide.nama }}</a></strong
          ><br>{{ ide.umur }}
        </p>
  </div>
</template>

<script>
export default {
  name: "idecard",
  data() {
    return {
      ide: [

         { nama: "ayus", umur: 212, gambar: "https://kisahtani.com/wp-content/uploads/2020/11/avocado-3210885_1920.jpg", category: "Nasi", price: "30.000" },
                  { nama: "bast", umur: 242, gambar: "https://kisahtani.com/wp-content/uploads/2020/11/green-beans-1018624_1920.jpg", category: "Rempah",  price: "5.000" },
                  { nama: "asada", umur: 642, gambar: "https://kisahtani.com/wp-content/uploads/2020/07/bawang-bombai.jpg", category: "Nasi", price: "10.000" },
                  { nama: "asdsad", umur: 223, gambar:  "https://kisahtani.com/wp-content/uploads/2020/07/bawang-putih.jpg", category: "Rempah",  price: "30.000" },
      ],
      search: '',
    };
  },
};
 


</script>

<style>
/* Force scrollbars onto browser window */
</style>
