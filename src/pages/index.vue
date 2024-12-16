<template>
  <v-app>
    <v-app-bar :elevation="2">
      <template v-slot:prepend>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
      </template>

      <template #append>
        <v-btn class="mr-2">
          <v-badge dot color="info">
            <v-icon icon="mdi-bell-outline"></v-icon>
          </v-badge>
        </v-btn>

        <v-avatar>
          <v-img cover src="data:image/jpeg;base64,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"></v-img>
        </v-avatar>
      </template>

      <v-app-bar-title>Meu app</v-app-bar-title>
    </v-app-bar>

    <v-main>
      <v-container>
        <h1>Dashboard</h1>

        <v-row>
          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end"
                src="https://images.pexels.com/photos/29354790/pexels-photo-29354790/free-photo-of-farol-de-salvador.jpeg?auto=compress&cs=tinysrgb&w=600"
              >
                <v-card-title>Top 10 Praias na Bahia</v-card-title>
              </v-img>

              <v-card-subtitle class="pt-3">Salvador</v-card-subtitle>

              <v-card-text>
                <div>Igreja Colonial Encantadora</div>

                <div>Em Riverside</div>
              </v-card-text>
              <v-card-actions>
                <v-btn color="primary" variant="outlined">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" color="blue" variant="tonal">Comprar</v-btn>
              </v-card-actions>
            </v-card>

            <v-card flat class="border">
              <v-img
                class="align-end"
                src="https://images.pexels.com/photos/29354790/pexels-photo-29354790/free-photo-of-farol-de-salvador.jpeg?auto=compress&cs=tinysrgb&w=600"
              >
                <v-card-title>Top 10 Praias na Bahia</v-card-title>
              </v-img>

              <v-card-subtitle class="pt-3">Salvador</v-card-subtitle>

              <v-card-text>
                <div>Igreja Colonial Encantadora</div>

                <div>Em Riverside</div>
              </v-card-text>
              <v-card-actions>
                <v-btn color="primary" variant="outlined">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" color="blue" variant="tonal">Comprar</v-btn>
              </v-card-actions>
            </v-card>

            <v-card flat class="border">
              <v-img
                class="align-end"
                src="https://images.pexels.com/photos/29354790/pexels-photo-29354790/free-photo-of-farol-de-salvador.jpeg?auto=compress&cs=tinysrgb&w=600"
              >
                <v-card-title>Top 10 Praias na Bahia</v-card-title>
              </v-img>

              <v-card-subtitle class="pt-3">Salvador</v-card-subtitle>

              <v-card-text>
                <div>Igreja Colonial Encantadora</div>

                <div>Em Riverside</div>
              </v-card-text>
              <v-card-actions>
                <v-btn color="primary" variant="outlined">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" color="blue" variant="tonal">Comprar</v-btn>
              </v-card-actions>
            </v-card>
            <v-card flat class="border">
              <v-img
                class="align-end"
                src="https://images.pexels.com/photos/29354790/pexels-photo-29354790/free-photo-of-farol-de-salvador.jpeg?auto=compress&cs=tinysrgb&w=600"
              >
                <v-card-title>Top 10 Praias na Bahia</v-card-title>
              </v-img>

              <v-card-subtitle class="pt-3">Salvador</v-card-subtitle>

              <v-card-text>
                <div>Igreja Colonial Encantadora</div>

                <div>Em Riverside</div>
              </v-card-text>
              <v-card-actions>
                <v-btn color="primary" variant="outlined">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" color="blue" variant="tonal">Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script lang="ts" setup>
  //
</script>
