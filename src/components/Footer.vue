<template>
  <v-footer padless>
      <v-col lg="12">
          <v-row justify="center">
              <v-col lg="4" class="text-center">
                  <v-toolbar-title>V App</v-toolbar-title>
                        <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 black--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>
      <v-subheader>Lorem ipsum dolor sit amet consectetur adipisicing elit.</v-subheader>
      <v-form class="mt-4">
          <v-text-field label="Email" outlined dense></v-text-field>
          <v-btn rounded color="success">Subscribe us</v-btn>
      </v-form>
              </v-col>
          </v-row>
                       <div class="mt-10" >
                  <v-divider></v-divider>
                  <v-subheader justify-center> Developed by Vlad Bulgakov  {{ new Date().getFullYear() }} — <strong> made with ♥</strong>
                  <v-spacer></v-spacer>
                  </v-subheader>
              </div>
      </v-col>
   
  </v-footer>
</template>

<script>
  export default {
    name: "Footer",
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>
<style >
.v-toolbar__title {
    font-size: 32px;
    color: #4caf50;
    font-weight: 700;
    font-family: cursive;
}
</style>