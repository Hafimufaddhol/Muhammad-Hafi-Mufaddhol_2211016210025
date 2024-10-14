<template>
  <v-app id="inspire">
    <v-app-bar flat>
      <v-container class="mx-auto d-flex align-center justify-center">
        <v-avatar class="me-4" color="grey-darken-1" size="32">
          <v-icon icon="mdi-account-circle"></v-icon>
        </v-avatar>

        <v-btn
          v-for="link in links"
          :key="link"
          :text="link"
          variant="text"
        ></v-btn>

        <v-spacer></v-spacer>

        <v-responsive max-width="160">
          <v-text-field
            density="compact"
            label="Search"
            rounded="lg"
            variant="solo-filled"
            flat
            hide-details
            single-line
          ></v-text-field>
        </v-responsive>
      </v-container>
    </v-app-bar>

    <v-main class="bg-grey-lighten-3">
      <v-container>
        <v-row>
          <v-col cols="2">
            <v-sheet rounded="lg">
              <v-list rounded="lg">
                <v-list-item
                  v-for="(platform, index) in platforms"
                  :key="index"
                  :title="platform.title"
                  :href="platform.link"
                  link
                ></v-list-item>
              </v-list>
            </v-sheet>
          </v-col>

          <v-col>
            <v-sheet
              min-height="70vh"
              rounded="lg"
            >
              <!--  -->
              <v-img
              height="100%"
              width="100%"
              aspect-ratio="16/9"
              src="@/assets/Kelinci.jpg"
              rounded="lg"
              >
              <div style="width: 100%; height: 100%; background: linear-gradient(to bottom, rgba(33, 33, 33, 0) 0%, rgba(33, 33, 33, 1) 100%); display: flex; align-items: flex-end; justify-content: center;"></div>
            </v-img>


            <v-card-title class="text-h6 text-md-h5 text-lg-h4 mt-5">DIJUAL!</v-card-title>
      <v-card-text>
        Kelinci Beserta Kandangnya
        jika Minat Hubugi lewat link disamping
      </v-card-text>
          </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
// const links = ["Dashboard", "Messages", "Profile", "Updates"];
</script>

<script>
export default {
  data: () => ({
    links: ["Dashboard", "Messages", "Profile", "Updates"],
    platforms: [
      { title: "YouTube", link: "https://www.youtube.com" },
      { title: "Twitter", link: "https://www.twitter.com" },
      { title: "Instagram", link: "https://www.instagram.com" },
      { title: "Facebook", link: "https://www.facebook.com" },
    ],
  }),
};
</script>
