<template>
    <div class="select">
      Seleziona un genere musicale:
      <!-- $emit manda il valore della selezione al componente padre per generare solo gli elementi selezionati -->
      <select name="genre" id="genre" v-model="userSelect" @change="$emit('selectedGenre', userSelect)">
        <option value="all">Tutti</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </div>
</template>

<script>
    export default {
    name: 'GenreSelection',
        data() {
            return {
                // valore della selezione
                userSelect : '',
            }
        }
    }
</script>

<style scoped lang="scss">
.select {
    margin: 30px 0;
    text-align: center;
    color: white;
    #genre {
      margin: 0 10px;
    }
  }
</style>
