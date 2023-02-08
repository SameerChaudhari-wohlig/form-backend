<template>
  <v-app>
    <v-app-bar title="Instagram" class="px-5">
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-text-field class="pad" size="1" rounded placeholder="Search" v-model="name"><v-btn icon="mdi-magnify"></v-btn>
      </v-text-field>
    </v-app-bar>
    <!-- <pre>{{ posts }}</pre> -->
    <v-main class="my-8">
      <table class="table caption-top">

        <thead>
          <tr class="table-primary">
            <!-- <th scope="col" >ID</th> -->
            <th scope="col">Name</th>
            <th scope="col">Age</th>
            <!-- <th scope="col">BloodGroup</th> -->
            <th scope="col">Gender</th>
            <!-- <th scope="col">Subject</th> -->
            <!-- <th scope="col">ranking</th> -->
          </tr>
          <tr class="table-info" v-for="post in posts" :key="post.id">
            <!-- <td >{{ Product.id }}</td> -->
            <td>{{ post.name }}</td>
            <td>{{ post.age }}</td>
            <!-- <td>{{ Product.Bloodgroup }}</td> -->
            <td>{{ post.gender }}</td>
            <!-- <td>{{ Product.subject }}</td> -->
            <!-- <td>{{ Product.ranking }}</td> -->
          </tr>
        </thead>
      </table>

      <!-- <v-row>
        <v-col cols="6">
          <v-card class="mx-auto" max-width="344">
  
            <h3 class="mt-4">{{ Product.name }}</h3>
            <v-btn icon="mdi-cards-heart"></v-btn>
            <v-btn icon="mdi-comment"></v-btn>
            <v-btn icon="mdi-share"></v-btn>
            <v-card-title>
              UserName : {{ Product.age }}</v-card-title
            >
            <h3>{{ Product.gender }} </h3>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row> -->
    </v-main>
  </v-app>
</template>

<script setup>
// import { ref } from "vue";
// import data from "../data";
// const Products = ref(data);

const url = "http://localhost:3001/student"

let posts = ref([]);
const { data } = await useFetch(url);
posts = data;

</script>
