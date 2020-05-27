<script>
  import randomInteger from '../utils/randomInterger';

  let text;

  function generateNewFact() {
    fetch('https://cat-fact.herokuapp.com/facts')
      .then(res => res.json())
      .then(data => {
          const max = data.all.length;
          const index = randomInteger(0, max);
          text = data.all[index].text;
          console.log(text);
        });
  };

  generateNewFact();
</script>

<style>
  h2 {
    background-color: var(--dark-color3);
    padding: 16px;
    margin-right: 16px;
  }

  .fact {
    display: flex;
    width: 100%;
    justify-content: center;
  }

  button {
    border: none;
    cursor: pointer;
    min-width: 150px;
    outline: none;
    font-weight: bold;
    font-size: 1.2rem;
    background-color: var(--green);
  }

  button:hover {
    filter: brightness(110%);
  }

  button:active {
    filter: brightness(100%);
  }

  @media (max-width: 768px) {
    .fact {
      flex-direction: column;
      margin-top: calc(100% - 50%)
    }

    h2 {
      margin-right: initial;
      font-size: 1.1rem;
      padding: 8px;
      margin-bottom: 8px;
    }

    button {
      padding: 8px;
      font-size: 1.2rem;
    }
  }
</style>

<div class='fact'>
  <h2>{text || 'loading'}</h2>
  <button on:click={generateNewFact}>NEW FACT!</button>
</div>