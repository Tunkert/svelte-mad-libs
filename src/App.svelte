
<script>
  let name = '';
  let occupation = '';
  let favoritePlace = '';
  let action = '';
  let landPlace = '';
  let animal = '';
  let madLibsPar = 'madLibsPar';
  import MadLibsParagraph from './MadLibsParagraph.svelte'
  function displayBlockFunc() {
    const madLibsPar = document.getElementById("madLibsPar");
    madLibsPar.classList.remove("d-none");
  }
</script>

<main>
  <h1>MadLibs Fun!</h1>
  <div class="inputs-container">
    <div class="input-wrapper">
      <div class="input-flex">
        <label for="name">Enter your name: </label>
        <input type="text" id="name" bind:value="{name}">
      </div>
    </div>
    <div class="input-wrapper">
      <div class="input-flex">
        <label for="occupation">Enter your occupation: </label>
        <input type="text" id="occupation" bind:value="{occupation}">
      </div>
    </div>
    <div class="input-wrapper">
      <div class="input-flex">
        <label for="favorite-place">Enter your favorite place: </label>
        <input type="text" id="favorite-place" bind:value="{favoritePlace}">
      </div>
    </div>
    <div class="input-wrapper">
      <div class="input-flex">
        <label for="action">Enter an action: </label>
        <input type="text" id="action" bind:value="{action}">
      </div>
    </div>
    <div class="input-wrapper">
      <div class="input-flex">
        <label for="landPlace">Enter a land place type: </label>
        <input type="text" id="landPlace" bind:value="{landPlace}">
      </div>
    </div>
    <div class="input-wrapper">
      <div class="input-flex">
        <label for="animal">Enter an animal (plural): </label>
        <input type="text" id="animal" bind:value="{animal}">
      </div>
    </div>
    <div class="button-container">
      <button on:click="{displayBlockFunc}">Read Your Mad Lib!</button>
    </div>
  </div>
  <MadLibsParagraph charPar="{madLibsPar}" charName="{name}" charJob="{occupation}" charPlace="{favoritePlace}" charAction="{action}" charLandPlace="{landPlace}" charAnimal="{animal}"/>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Lato:wght@400;700&display=swap');  
  main {
    font-family: 'Lato', sans-serif;
  }
  .inputs-container {
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid rgba(0, 0, 0, 0.7);
    border-radius: 5px;
    box-shadow: 1px 2px 2px 1px rgba(0, 0, 0, 0.7);
    background-color: #f4efef;
  }
  .input-wrapper {
    display: flex;
    flex-direction: column;
    margin-bottom: 10px;
  }
  .input-flex {
    display: flex;
    justify-content: space-between;
  }
  /*.inputs-container input {

  }*/
  h1 {
    color: rgba(0, 0, 0, 0.7);
    text-transform: uppercase;
    text-align: center;
    letter-spacing: 0.1em;
  }
  label {
    cursor: pointer;
  }
  input {
    padding: 5px 10px;
    border: 1px solid rgba(0, 0, 0, 0.7);
    border-radius: 5px;
  }
  .button-container {
    display: flex;
    justify-content: center;
  }
  button {
    padding: 10px 20px;
    border-radius: 5px;
    border: 1px solid rgba(0, 0, 0, 0.7);
    cursor: pointer;
    text-transform: uppercase;
    font-family: inherit;
    background: linear-gradient(to right, #33d657, #78e37b);
  }
  button:hover {
    background: linear-gradient(to right,#78e37b ,#a1f5a4);
  }
</style>
