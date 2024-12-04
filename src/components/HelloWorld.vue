<template>
  <v-container class="fill-height">
    <v-responsive
      class="align-centerfill-height mx-auto"
      max-width="900"
    >
      <v-img
        class="mb-4"
        height="150"
        src=""
      />

      <div class="text-center ">
        <div class="text-body-4 font-weight-light mb-n1">Vuetify by</div>

        <h1 class="text-h2 font-weight-bold">Tiago Vieira</h1>

        <div class="py-2" />

        <v-tooltip text="8711000000">
          <template v-slot:activator="{ props }">
            <v-btn v-bind="props">Contato</v-btn>
          </template>
        </v-tooltip>
      </div>

      <div class="py-4" />

      <v-row>
        <v-col cols="6">
          <v-card
            append-icon="mdi-open-in-new"
            class="py-4"
            color="surface-variant"
            href="https://www.linkedin.com/in/tiago-svieira/"
            prepend-icon="mdi-linkedin"
            rel="noopener noreferrer"
            rounded="lg"
            subtitle="Minha rede social de trabalho"
            target="_blank"
            title="LinkedIn"
            variant="text"
          >
            <v-overlay
              opacity=".06"
              scrim="primary"
              contained
              model-value
              persistent
            />
          </v-card>
        </v-col>

        <v-col cols="6">
          <v-card
            append-icon="mdi-open-in-new"
            class="py-4"
            color="surface-variant"
            href="https://tiagosvieira.com.br/"
            prepend-icon="mdi-web"
            rel="noopener noreferrer"
            rounded="lg"
            subtitle="Site pessoal e Portfólio"
            target="_blank"
            title="Website"
            variant="text"
          >
            <v-overlay
              opacity=".06"
              scrim="primary"
              contained
              model-value
              persistent
            />
          </v-card>
        </v-col>

        <v-col cols="6">
          <v-card
            append-icon="mdi-open-in-new"
            class="py-4"
            color="surface-variant"
            href="https://github.com/tiagosvieira10"
            prepend-icon="mdi-github"
            rel="noopener noreferrer"
            rounded="lg"
            subtitle="Meus códigos já realizados"
            target="_blank"
            title="GitHub"
            variant="text"
          >
            <v-overlay
              opacity=".06"
              scrim="primary"
              contained
              model-value
              persistent
            />
          </v-card>
        </v-col>

        <v-col cols="6">
          <v-card
            append-icon="mdi-open-in-new"
            class="py-4"
            color="surface-variant"
            href="https://lift.app.br/"
            prepend-icon="mdi-rocket"
            rel="noopener noreferrer"
            rounded="lg"
            subtitle="Conheça um pouco sobre meu trabalho Freelancer"
            target="_blank"
            title="Lift."
            variant="text"
          >
            <v-overlay
              opacity=".06"
              scrim="primary"
              contained
              model-value
              persistent
            />
          </v-card>
        </v-col>
      </v-row>
    </v-responsive>
  </v-container>
</template>

<script setup lang="ts">
  //
</script>
