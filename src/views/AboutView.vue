<template>
    <div class="about pa-6">
      <v-row align-contents="center">
    <v-col>
    <h1>H1テキスト</h1>
    <p>テキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキスト</p>
  </v-col>
    <v-btn>ボタン</v-btn>
  </v-row>
  <v-card outlined>
    <v-data-table
      :headers="headers"
      :items="desserts"
      :search="search"
    ></v-data-table>
  </v-card>
    </div>
</template>

<script>
</script>