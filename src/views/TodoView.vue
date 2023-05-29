<template>
  <div class="about pa-6">
    <!--
    <h1>H1テキスト</h1>
    <p>テキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキスト</p>
  -->
  <v-card outlined>
    <v-card-title>
      Nutrition
      <v-spacer></v-spacer>
      <v-row
      align-items="center">
        <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
      <v-btn>ボタン</v-btn>
      </v-row>
    </v-card-title>
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
