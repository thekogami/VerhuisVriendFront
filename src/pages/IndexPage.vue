<template>
  <q-page class="flex flex-center">
    <div class="text-center">
      <img
        alt="Quasar logo"
        src="~assets/quasar-logo-vertical.svg"
        style="width: 200px; height: 200px"
      />
      <div class="q-mt-lg">
        <router-link to="/login">
          <q-btn label="Ga naar de inlogpagina" color="primary" />
        </router-link>
      </div>
    </div>
  </q-page>
</template>

<script setup>
defineOptions({
  name: "IndexPage",
});
</script>
