<template>
  <div class="subscribe">
    <div class="description text-center">
      <h2>Subscribe and Receive A Free eBook</h2>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. <br/> Quam mollitia</p>
    </div>

    <div class="input-group input-container mb-3">
      <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="button-addon2">
      <button class="btn btn-outline-secondary" type="button" id="button-addon2">SUBSCRIBE</button>
    </div>
    <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </div>
</template>

<script>
export default {
  name: 'Subscribe'
}
</script>

<style lang="scss">
.subscribe{
  width: 100%;
  height: 70vh;
  background-color: grey;
  .input-container{
    max-width: 500px;
    margin: 0 auto;
  }
}
</style>