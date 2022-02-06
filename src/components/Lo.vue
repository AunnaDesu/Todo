<template>
  <v-container>
    <v-card
      class="mx-auto"
      max-width="344"
      v-for="(item, index) in A1"
      :key="index"
    >
    
    <div class="">{{item.name}}</div>
    <v-btn
      class="mx-2"
      fab
      dark
      small
      color="primary"
      @click="deleteTodo(index)"
    >
      <v-icon dark>
        mdi-minus
      </v-icon>
    </v-btn>
    
    
    
    </v-card>
  </v-container>
</template>

<script>
export default {
     props: ["A1"],
  methods: {
     deleteTodo(index) {
      this.A1.splice(index, 1);
    },
  },
};
</script>

<style>
</style>
//Excel