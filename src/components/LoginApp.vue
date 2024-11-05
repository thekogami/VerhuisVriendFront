<template>
  <q-page class="flex flex-center login-page">
    <q-card style="width: 400px; max-width: 90vw;">
      <q-card-section>
        <div class="text-h5 text-primary text-center">Welkom bij VerhuisVriend</div>
        <div class="text-subtitle2 text-center text-grey-7 q-mt-xs">
          Eenvoudig. Slim. Efficiënt.
        </div>
        <div class="text-body2 text-center text-grey-6 q-mt-sm">
          Begin nu met plannen van uw verhuizing.
        </div>
      </q-card-section>

      <q-card-section>
        <q-input
          v-model="email"
          type="email"
          label="E-mailadres"
          outlined
          clearable
          dense
        />
        <q-input
          v-model="password"
          type="password"
          label="Wachtwoord"
          outlined
          clearable
          dense
          class="q-mt-md"
        />
      </q-card-section>

      <q-card-actions align="center">
        <q-btn
          label="Inloggen"
          color="primary"
          @click="handleLogin"
          :loading="loading"
          style="width: 100%;"
        />
        <q-btn
          flat
          label="Account aanmaken"
          color="primary"
          class="q-mt-sm"
          @click="navigateToSignup"
        />
      </q-card-actions>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: "LoginApp",
  data() {
    return {
      email: "",
      password: "",
      loading: false,
    };
  },
  methods: {
    handleLogin() {
      this.loading = true;
      // Simuleer authenticatie - vervang dit met een echte API-aanroep
      setTimeout(() => {
        this.loading = false;
        alert("Succesvol ingelogd! Welkom bij VerhuisVriend.");
      }, 1000);
    },
    navigateToSignup() {
      // Navigeren naar de aanmaakpagina van het account
      this.$router.push("/signup");
    },
  },
};
</script>

<style scoped>
.login-page {
  background: #f5f5f5;
}
</style>