<template>
          <v-flex xs12>
            <v-card color="blue-grey " class="white--text">
              <v-card-title primary-title>
                <div>
                  <div class="headline">{{Name}}</div>
                  <span>{{Clave}}</span> 
                  <hr>
                  <span>{{Semestre}}</span>
                  <hr>
                </div>
              </v-card-title>
              <v-card-text>
                <span v-html="Descripcion">
                  </span><br>
                  <hr>
                  <table >
                    <th>{{HE}}</th>
                    <th>{{HP}}</th>
                    <th>{{suma(HE,HP)}}</th>
                  </table>
                  <hr>
              </v-card-text>
              <v-card-actions>
                <v-btn flat dark>Listen now</v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
</template>
<script>
export default {
    name:"Matter",
    props:{
      Name:String,
      Clave:String,
      Descripcion:String,
      HE:String,
      HP:String,
      Archivo:String,
      Semestre:String
    },
    methods:{
      suma(HE,HP){
        return parseInt(HE,10)+parseInt(HP,10) 
      }
    }

}
</script>
