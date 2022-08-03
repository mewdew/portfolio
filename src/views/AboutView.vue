<template>
  <div class="about">
    <div class="leftSection">
      <div class="picture">
        <img
          alt="Shivangi Sinha"
          class="picture"
          src="../assets/pic.jpg"
          width="inherit"
          height="inherit"
        />
      </div>
      <div class="links"></div>
    </div>
    <div class="rightSection">
      <h2>Hello There!</h2>
      <p>
        My name is Shivangi Sinha. I'm a Frontend Developer by profession with
        affinity for all things art.
      </p>
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    display: flex;
    height: calc(100vh - 61px);
    align-items: center;
    justify-content: space-around;
    padding: 1rem;
    background: #c5cce9; /* Old browsers */
    background: -moz-linear-gradient(
      top,
      #c5cce9 0%,
      #c5cce9 33%,
      #efe3ef 33%,
      #efe3ef 66%,
      #eec7c8 66%,
      #eec7c8 100%
    ); /* FF3.6-15 */
    background: -webkit-linear-gradient(
      top,
      #c5cce9 0%,
      #c5cce9 33%,
      #efe3ef 33%,
      #efe3ef 66%,
      #eec7c8 66%,
      #eec7c8 100%
    ); /* Chrome10-25,Safari5.1-6 */
    background: linear-gradient(
      to bottom,
      #c5cce9 0%,
      #c5cce9 33%,
      #efe3ef 33%,
      #efe3ef 66%,
      #eec7c8 66%,
      #eec7c8 100%
    ); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#c5cce9', endColorstr='#eec7c8',GradientType=0 );
  }

  .leftSection {
    display: flex;
    max-width: 50%;
    flex-direction: column;
  }

  .picture {
    max-height: 50vh;
  }

  img {
    position: relative;
    max-height: 100%;
  }
}
</style>
