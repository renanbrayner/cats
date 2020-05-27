<script>
  import randomInterger from '../utils/randomInterger';
  import Cat from 'svelte-icons/fa/FaCat.svelte';

  // --red: #BF616A;
	// --orange: #D08770;
	// --yellow: #EBCB8B;
	// --green: #A3BE8C;
  // --purple: #B48EAD;
  
  let random = randomInterger(0, 4);
  let color;

  function handleMouseOver() {
    random = randomInterger(0, 4);
      switch (random) {
    case 0:
      color = '#BF616A';
      break;
    case 1:
      color = '#D08770';
      break;
    case 2:
      color = '#EBCB8B';
      break;
    case 3:
      color = '#A3BE8C';
      break;
    case 4:
      color = '#B48EAD';
      break;
    };
  }

  handleMouseOver();
</script>

<style>
  nav {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    width: 72px;
    background-color: var(--dark-color1);

    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .logo {
    width: 100%;
    height: 72px;
  }

  h1 {
    margin-top: 16px;
    font-size: 2rem
  }
</style>

<nav>
  <div style='background: {color}' class="logo" on:mouseover={handleMouseOver} on:load={handleMouseOver}>
    <Cat />
  </div>
  <h1 style='color: {color}'>
  C<br/>
  A<br/>
  T<br/>
  S<br/>
  !
  </h1>
</nav>