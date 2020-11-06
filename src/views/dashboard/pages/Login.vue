<template>
  <main class="clickable">
    <v-content>
      <v-container class="fill-height">
        <v-row
          align="center"
          justify="center"
        >
          <v-col class="">
            <div class="display-1 mb-3">
              <v-icon
                class="mr-2"
                large="large"
              /> My ProTiming
            </div>
            <v-card light="light">
              <v-card-text>
                <v-form
                  class="login"
                  @click.prevent="login"
                >
                  <v-text-field
                    v-model="username"
                    light="light"
                    prepend-icon="person"
                    label="Username"
                    required
                  />
                  <v-text-field
                    v-model="password"
                    light="light"
                    prepend-icon="lock"
                    label="Password"
                    type="password"
                    required
                  />
                  <p
                    v-if="error"
                    class="error"
                  >
                    Has introducido mal el email o la contraseña.
                  </p>
                  <v-btn
                    block="block"
                    type="submit"
                  >
                    Sign in
                  </v-btn>
                </v-form>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </main>
</template>

<script>
  export default {
    data: () => ({
      username: '',
      password: '',
      error: false,
    }),
    methods: {

    },
  }
</script>

<style>
#app {
  background-image: url("https://images.unsplash.com/photo-1497733942558-e74c87ef89db?dpr=1&auto=compress,format&fit=crop&w=1650&h=&q=80&cs=tinysrgb&crop=");
  background-size: cover;
  overflow: hidden;
}

</style>
