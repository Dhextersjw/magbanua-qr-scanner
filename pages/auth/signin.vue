<template>

  <div class="d-flex mx-auto justify-center align-center" style="height: 88vh;">

   

    <v-card width="500" 
      class="mx-auto pa-12 pb-8"
      elevation="8"
      max-width="448"
      rounded="lg"
    >
    <h1>

    </h1>
      <div class="text-subtitle-1">Login</div>

      <v-text-field
        density="compact"
        placeholder="Email address"
        prepend-inner-icon="mdi-email-outline"
        variant="outlined"
      ></v-text-field>

      <div class="text-subtitle-2 text-medium-emphasis d-flex align-center justify-space-between">
        Password

      
      </div>

      <v-text-field
        :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
        :type="visible ? 'text' : 'password'"
        density="compact"
        placeholder="Enter your password"
        prepend-inner-icon="mdi-lock-outline"
        variant="outlined"
        @click:append-inner="visible = !visible"
      ></v-text-field>

      <v-card
        class="mb-12"
        color="surface-variant"
        variant="tonal"
      >
        
      </v-card>

      <v-btn
        class="mb-8"
        color="blue"
        size="large"
        variant="tonal"
        block rounded
      >
        sign-in 
      </v-btn>

      <v-card-text class="text-center">
        <v-btn style="background-color: red; opacity: 90%;" width="10vh" @click="signInWithGoogle()" block rounded>
        <a
          class="text-blue text-decoration-none"
          href="#"
          rel="noopener noreferrer"
          target="_blank"
          style="color: white;"
          
          
        >
          Sign in with Google <v-icon icon="mdi-chevron-right"></v-icon>
        </a>
        </v-btn>
      </v-card-text>
    </v-card>
  </div>
</template>

<style>
.text-subtitle-1 {
margin-left: 150px;
}
</style>

<script>
export default {
  layout: "auth",
  middleware: ['auth'],
  methods: {
    signInWithGoogle(){
      this.$auth.loginWith('google')
    }

  }




}

</script>