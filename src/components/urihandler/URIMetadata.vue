<template>
  <v-layout xs12 column class="info-card">
    <v-flex xs12>
      <v-card elevation="0">
       <v-card-title class="monospaced">
           <div>
          <span class="monospaced bold">Raw URI Data:</span>
          {{ uri.data }}
           </div>

           <div>
            <span class="monospaced bold">Full Link:</span>
              {{ uri.build() }}
           </div>
       </v-card-title> 
      </v-card>
      </v-flex>
    </v-layout>
</template>


<script>

    import { TransactionURI } from 'nem2-uri-scheme';

export default {

    props: {
        uri: TransactionURI
    },
}
</script>

<style scoped>
 .info-card {
     overflow: scroll;
 }
</style>