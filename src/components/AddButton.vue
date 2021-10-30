<template>
    <div class="btn-container">
        <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
                <v-btn
                    class="mx-2"
                    fab
                    small
                    dark
                    v-bind="attrs"
                    v-on="on"
                    >
                    <v-icon dark>
                        mdi-plus
                    </v-icon>
                </v-btn>
            </template>
            <span> {{ tooltip }} </span>
        </v-tooltip>
    </div>
</template>

<script>
  export default {
      props: {
          tooltip: String
    }
  }
</script>

<style scoped lang="scss">
    .btn-container {
        margin-top: 10px;
        float: right;
    }
</style>