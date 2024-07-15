<template>
  <div class="oculta">
    <img
      :src="pokemon.image"
      :alt="pokemon.name"
      :class="{ 'blurred': !pokemon.guessed, 'guessed': pokemon.guessed }"
      class="img-fluid"
    />
    <div v-if="!pokemon.guessed">
      <input type="text" v-model="guessInput" @keyup.enter="makeGuess" placeholder="Ingrese el nombre"> <br>
      <button @click="makeGuess">Descubrir</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PokeCard',
  props: {
    pokemon: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      guessInput: '',
    };
  },
  methods: {
    makeGuess() {
      this.$emit('guess', this.pokemon, this.guessInput);
    }
  },
};
</script>

<style scoped>
.blurred {
  filter:  grayscale(100%) blur(5px);
}

.guessed {
  filter: none; /* Elimina cualquier filtro si el Pokémon ha sido adivinado */
}

input {
  font-size: 10px;
  border-radius: 5px;
  margin-bottom: 0.5rem;
}

button {
  margin-top: 5px;
  background-color: #FFCB03;
  border-color: #335CA6;
  border-radius: 50px;
  border-width: medium;
  color: #335CA6;
  font-weight: bolder;
  padding: 10px;
}

img {
  height: 12rem;
}

.oculta {
  height: 21rem;
}
</style>