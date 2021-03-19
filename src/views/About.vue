<template>
  <div class="about">
    <h1 class="d-flex justify-center pt-15">Aplicativo para controle de tarefas</h1>
    <div class="d-flex justify-center pt-15">
      <v-btn
      color="blue-grey"
      class="ma-2 white--text"
      v-for="social in socialMedia"
      :key="social.title"
      :to="socialMedia.to"
    >
      {{ social.title }}
      <v-icon
        right
        dark
      >
        {{ social.icon }}
      </v-icon>
    </v-btn>
    </div>
  </div>
</template>
<script>
export default {
    data: () => ({
       socialMedia: [
          { title: 'Instagram', icon: 'mdi-instagram', to: '/' },
          { title: 'Github', icon: 'mdi-github', to: '/about' },
          { title: 'Linkedin', icon: 'mdi-linkedin', to: '/about' }
        ]
       }),
  }
</script>

