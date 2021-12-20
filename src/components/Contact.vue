<template>
    <v-container class = "my-15">
     <v-row justify="center">
      <v-col lg="12" class="text-center">
       <v-subheader class="text-h4 justify-center">Contact</v-subheader>
         <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis, molestiae!</p>
        </v-col>
        <v-col lg="6">
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d84400.0883664232!2d22.209597949178345!3d48.619360516083034!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x473919b944b6e3d9%3A0xda6ae0130042a3c!2z0KPQttCz0L7RgNC-0LQsINCX0LDQutCw0YDQv9Cw0YLRgdC60LDRjyDQvtCx0LvQsNGB0YLRjA!5e0!3m2!1sru!2sua!4v1639601794037!5m2!1sru!2sua" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
        </v-col>
        <v-col lg ="6">
            <v-form ref="form" >
    <v-text-field
      v-model="conatctInfo.name"
      :counter="10"
      label="Name"
      required
    ></v-text-field>

    <v-text-field
      v-model="conatctInfo.email"
      label="E-mail"
      required
    ></v-text-field>
    <v-textarea label="Massage" v-model="conatctInfo.message"></v-textarea>



    <v-btn  color="success" class="mr-4" > Send</v-btn>
  </v-form>
        </v-col>
       </v-row>
    </v-container>

</template>

<script>
export default{
    name: "Contact",
    data() {
        return {
            conatctInfo:{

            }
        }
    },
}
</script>

<style scoped>
</style>