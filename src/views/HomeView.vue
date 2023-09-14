<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row justify="center">
          <v-col cols="12" sm="8" md="6">
            <v-card>
              <v-card-title class="text-center">Inicio de Sesión</v-card-title>
              <v-card-text>
                <v-form @submit.prevent="login">
                  <v-text-field
                    v-model="email"
                    label="Correo Electrónico"
                    required
                  ></v-text-field>
                  <v-text-field
                    v-model="password"
                    label="Contraseña"
                    type="password"
                    required
                  ></v-text-field>
                  <v-btn
                    color="primary"
                    block
                    type="submit"
                  >
                    Iniciar Sesión
                  </v-btn>
                </v-form>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: ''
    };
  },
  methods: {
    login() {
      // Aquí puedes agregar la lógica de inicio de sesión
      // Puedes usar Firebase Authentication u otro servicio de autenticación.
    }
  }
};
</script>

<style scoped lang="scss">
.login-card {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
}

.login-title {
  font-size: 24px;
  text-align: center;
  margin-bottom: 20px;
}

.login-button {
  margin-top: 20px;
}

</style>