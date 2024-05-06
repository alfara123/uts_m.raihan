<template>
        <v-navigation-drawer
          expand-on-hover
          rail
        >
          <v-list>
            <v-list-item
              prepend-avatar="https://th.bing.com/th/id/OIP.ePOE9pe2RM_2JgpMo66-_AHaFj?w=208&h=180&c=7&r=0&o=5&dpr=1.2&pid=1.7"
              subtitle="botakbolenang728@gmail.com"
              title="Muhammad Raihan Al Fara Kesuma"
            ></v-list-item>
          </v-list>
  
          <v-divider></v-divider>
  
          <v-list density="compact" nav>
            <v-list-item prepend-icon="mdi-folder" title="Home" :to="'/home'"></v-list-item>
            <v-list-item prepend-icon="mdi-account-multiple" title="Dosen" :to="'/dosen-entry'"></v-list-item>
            <v-list-item prepend-icon="mdi-star" title="Mahasiswa" :to="'/mahasiswa-entry'"></v-list-item>
            <v-list-item prepend-icon="mdi-star" title="Ruangan" :to="'/ruangan-entry'"></v-list-item>
          </v-list>
        </v-navigation-drawer>
  
        <v-main style="height: 250px"></v-main>
  </template>