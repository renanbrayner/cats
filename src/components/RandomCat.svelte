<script>
  let src;

  const getCatPhoto = () => {
    fetch('https://aws.random.cat/meow')
    .then(res => res.json())
    .then(data => src = data.file);
  }

  getCatPhoto();

  window.setInterval(function(){
    getCatPhoto();
  }, 6000);

</script>

<style>
  img {
    height: 50vh;
    width: auto;
  }

  .cats {
    height: 50vh;
    margin-bottom: 64px;
  }
</style>

<div class='cats'>
  <img src={src} alt='random cat'/>
</div>