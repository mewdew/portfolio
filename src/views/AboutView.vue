<template>
  <div class="about">
    <div class="leftSection">
      <div class="picture">
        <img alt="Shivangi Sinha" class="picture" src="../assets/pic.jpg" width="inherit" height="inherit" />
      </div>
    </div>
    <div class="rightSection">
      <h2>Hello There!</h2>
      <div class="context">
        <p>
          My name is Shivangi Sinha. I'm a Frontend Developer by profession with affinity for all things art.
        </p>
        <div class="links flexCol">
          <h3>Get in Touch</h3>
          <div class="icons flexRow">
            <span>
              <a href="https://www.facebook.com/shivangi.sinha.profile/">
                <img src="../assets/fb.svg" alt="fb" />
              </a>
            </span>
            <span>
              <a href="https://www.instagram.com/shivangi_sinha/">
                <img src="../assets/insta.svg" alt="insta" />
              </a>
            </span>
            <span>
              <a href="https://twitter.com/that_sinha">
                <img src="../assets/twitter.svg" alt="twitter" />
              </a>
            </span>
          </div>
        </div>
        <div class="mail">
          <a href="mailto:shivangisinha612@gmail.com">Drop a mail</a>
        </div>
        <div class="resumeLink">
          <a href="../assets/Resume_ShivangiSinha.pdf">Download Resume</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    display: flex;
    height: calc(100vh - 67px);
    align-items: center;
    justify-content: space-around;
    padding: 1rem;
    background: #c5cce9;
    /* Old browsers */
    background: -moz-linear-gradient(top,
        #c5cce9 0%,
        #c5cce9 33%,
        #efe3ef 33%,
        #efe3ef 66%,
        #eec7c8 66%,
        #eec7c8 100%);
    /* FF3.6-15 */
    background: -webkit-linear-gradient(top,
        #c5cce9 0%,
        #c5cce9 33%,
        #efe3ef 33%,
        #efe3ef 66%,
        #eec7c8 66%,
        #eec7c8 100%);
    /* Chrome10-25,Safari5.1-6 */
    background: linear-gradient(to bottom,
        #c5cce9 0%,
        #c5cce9 33%,
        #efe3ef 33%,
        #efe3ef 66%,
        #eec7c8 66%,
        #eec7c8 100%);
    /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
    filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#c5cce9', endColorstr='#eec7c8', GradientType=0);
  }

  .leftSection {
    display: flex;
    max-width: 50%;
    flex-direction: column;
    padding: 2rem;
    background: white;
    filter: drop-shadow(2px 4px 4px grey);
  }

  .rightSection {
    padding: 2rem;
    background: white;
    filter: drop-shadow(2px 4px 4px grey);
  }

  .picture {
    max-height: 50vh;
  }

  img {
    position: relative;
    max-height: 100%;
  }

  .links {
    padding-top: 2rem;
  }

  .resumeLink, .mail {
    padding-top: 1rem;
  }

  .icons span {
    padding-right: 1rem;
  }
  .icons a:hover {
    background-color: white;
  }
  .icons span img:hover {
    filter: drop-shadow(2px 4px 4px grey)
  }
}
</style>
