<template>
  <div class="hello">
    <div class="diceContainer">
      <div class="dice" key="dice2">
        <p class="person">{{who}}</p>
      </div>
      <div class="dice" key="dice2">
        <p>{{letter}}</p>
      </div>
      <div class="dice" key="dice3">
        <p>{{number}}</p>
      </div>
    </div>
    <button @click="generateRandom">aqui</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      who: "",
      letter: "",
      number: undefined,
      people: [
        "Yo",
        "Tu",
        "Mi Padre",
        "Mi Madre",
        "Nosotros",
        "Vosotros",
        "Mis Amigos"
      ],
      letters: [
        "A",
        "B",
        "C",
        "D",
        "E",
        "F",
        "G",
        "H",
        "I",
        "J",
        "K",
        "L",
        "M",
        "N",
        "O",
        "P",
        "Q",
        "R",
        "S",
        "T",
        "U",
        "V",
        "W",
        "X",
        "Y",
        "Z"
      ]
    };
  },
  methods: {
    generateRandom() {
      console.log("random");
      const randomIndex = Math.floor(Math.random() * this.letters.length);
      this.letter = this.letters[randomIndex];

      this.number = Math.floor(Math.random() * 27);
      const randomPersonIndex = Math.floor(Math.random() * this.people.length);

      this.who = this.people[randomPersonIndex];
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button {
  outline: none;
  border: none;
  background-color: #c60b1e;
  padding: 10px 20px;
  margin-top: 50px;
  color: white;
  font-size: 20px;
  border-radius: 10px;
  cursor: pointer;
  transition: 0.5s;
}

button:hover {
  transform: scale(1.1);
}
.diceContainer {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin: 0 20rem;
}
@media screen and (min-width: 400px) and (max-width: 1000px) {
  .diceContainer {
    margin: 0 10px;
  }
}

.dice {
  border: 1px solid rgba(53, 53, 53, 0.082);
  width: 200px;
  height: 200px;
  border-radius: 10px;
  font-size: 50px;
  background: #fff;
  box-shadow: inset 0 0 40px #ccc;
  border-radius: 40px;
}

p {
  line-height: 200px;
  margin: 0;
  color: #c60b1e;
}

.person {
  font-size: 60%;
}

@media screen and (max-width: 640px) {
  .diceContainer {
    display: flex;
    flex-direction: column;
    width: 200px;
    margin: 0 auto;
  }

  .dice {
    margin-top: 20px;
  }

  button {
    margin-bottom: 50px;
  }
}
</style>
