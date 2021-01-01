<template>
<div class="m-4">
      <p class="welcome text-center mt-4">
        Selamat datang di<br />
        <span class="page_title text-primary"><b>APLIKASI PERKREDITAN RAKYAT</b></span
        ><br />
        yaitu sebuah aplikasi kredit untuk produktif
      </p>

      <div>
        <div class="mb-3 bg-light p-3" align="center">
          <b-button block
            v-b-toggle pill
            size="lg"
            href="#example-collapse"
            @click.prevent
            class="bg-primary border-0 align-item-center"
            >Ajukan Pinjaman</b-button
          >
            <b-collapse id="example-collapse" class="m-4">
        
            <b-form @submit="onSubmit" @reset="onReset" v-if="show" class="bg-light">

              <b-form-group
                id="input-group-2"
                label-for="input-2"
              > <b-form-input
                  id="input-2"
                  v-model="form.name"
                  placeholder="Nominal Pinjaman"
                  required
                ></b-form-input>
              </b-form-group>

               <b-form-group
                id="input-group-3"
                label-for="input-3"
              > <b-form-select
                  id="input-3"
                  v-model="form.food"
                  :options="foods"
                  required
                ></b-form-select>
              </b-form-group>

              <b-form-group
                id="input-group-1"
                label-for="input-1"
              > <b-form-input
                  id="input-1"
                  v-model="form.email"
                  type="TextArea"
                  placeholder="Ringkasan Bisnis"
                  required
                ></b-form-input>
              </b-form-group>

                <b-form-group
                id="input-group-1"
                label-for="input-1"
              > <b-form-input
                  id="input-1"
                  v-model="form.email"
                  type="file"
                  placeholder="Upload File"
                  required
                ></b-form-input>
              </b-form-group>
              <b-button pill block type="submit" variant="warning">Submit</b-button>
             
            </b-form>
           
      
        </b-collapse>
        </div>
      </div>
    </div>
</template>
<script>
export default {
   
  name: "Hero",
    data() {
      return {
        form: {
          email: '',
          name: '',
          food: null,
          checked: []
        },
        foods: [{ text: 'pilih pelatihan', value: null }, 'diatas 10jt', 'dibawah 10jt', 'diatas 50jt', 'dibawah 50jt'],
        show: true
      }
    },
}
</script>
