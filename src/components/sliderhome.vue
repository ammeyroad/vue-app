<template>
  <div class="card shadow card-product"><br><br><br><br><br><br>
   
   <ul id="shomes">
  <li v-repeat="shome in shomes">
    {{shome.name}} - {{shome.email}}
  </li>
</ul>
  </div>
      

</template>

<script>
export default {
  name: "sliderhome", 
  props: ["shome"],
};
</script>

<style>
/* Force scrollbars onto browser window */
</style>
