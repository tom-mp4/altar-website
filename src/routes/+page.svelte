<script>
    import Marquee from "svelte-fast-marquee";
    let play = true;
</script>

<div class="page">
    <div class="top">
        <img src="/altar-white.png" alt="logo" class="logo">
        <a href="https://tom-mrt.fr" class="external-link">
            <div class="marquee-text">
                <div class="blur"></div>
                    <Marquee pauseOnHover={true} direction='right' speed={40} play={play}>
                        <h2>Discover our work ///Discover our work ///</h2>
                    </Marquee>
                <div style="rotate: 180deg" class="blur"></div>
            </div>
            <img class="arrow" src="/arrow.svg" alt="arrow">
        </a>
    </div>
    <div class="item1">
        <div class="box1">
            <div class="descriptor">
                <h2>Altar Collective</h2>
            </div>
            <div class="holograhpic">
                <img src="/stars.png" alt="stars">
            </div>
        </div>
        <div class="splitter"></div>
        <div class="box"></div>
    </div>
</div>

<style lang="scss">
  @import url("https://use.typekit.net/eqt5fok.css");
  @font-face {
    font-family: "Origin";
    src: local("Origin"),
    url("/fonts/origin-regular.otf") format("otf");
  }
  @font-face {
    font-family: "Joyride";
    src: local("Joyride"),
    url("/fonts/Joyride-ALT.otf") format("otf");
  }

  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(body) {
    min-height: 100vh;
    width: 100vw;
    background-color: #0E0E0E;
  }

  .page {
    display: flex;
    flex-direction: column;
    padding: 3vh;
    gap: 5rem;

    .top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 100%;
      gap: 5rem;

      .logo {
        width: 20%;
      }

      .external-link {
        display: flex;
        align-items: center;
        gap: 3rem;

        color: #0E0E0E;
        text-decoration: none;
        font-family: Origin, sans-serif;
        font-size: 36px;

        width: 80%;
        height: 10vw;
        padding: 3rem;

        background-color: #8C92AC;
        border-radius: 30px;

        .blur {
          z-index: 2;
          position: absolute;
          width: 10rem;
          height: 10vw;
          background: linear-gradient(to right, #8C92AC, transparent);
        }

        .arrow {
          height: 100%;
          transition: 0.3s ease;
        }

        &:hover {
          .arrow {
            transform: rotate(45deg);
          }
        }
      }
    }

    .item1 {
      display: flex;
      flex-direction: row;
      width: 60%;
      position: relative;

      .box1 {
        display: flex;
        flex-direction: column-reverse;
        align-items: end;

        background-image: url("/image.png");
        background-size: cover;

        height: 65vh;
        width: 45%;

        border-radius: 30px;

        .holograhpic {
          display: flex;
          align-items: center;
          justify-content: center;
          rotate: 45deg;
          z-index: 2;
          position: absolute;
          right: 87%;
          bottom: 25%;
          width: 6rem;
          height: 6rem;
          border-radius: 9999px;
          background-image: linear-gradient(
            to right,
            rgb(194, 255, 182),
            rgb(255, 163, 182),
            rgb(221, 169, 255),
            rgb(162, 209, 255)
          );

          img {
            width: 70%;
            height: 70%;
          }
        }

        .descriptor {
          display: flex;
          align-items: center;
          justify-content: center;
          background-color: #F2F2F2;
          width: 100%;
          height: 35%;
          border-radius: 30px;
          z-index: 1;
          padding: 2rem;

          h2 {
            font-family: Origin, sans-serif;
            font-size: 65px;
            text-align: center;
          }
        }
      }

      .box {
        background-color: #eee;
        padding: 2rem;

        min-height: 10rem;

        border-radius: 24px;
      }

      .splitter {
        background-color: #F2F2F2;

        width: 2rem;
        height: 100%;

        display: flex;
        flex-direction: column;
        justify-content: space-between;

        &::before {
          content: '';
          background-color: #0E0E0E;
          height: 45%;
          width: 2rem;

          border-radius: 0 0 30px 30px;
        }

        &::after {
          content: '';
          background-color: #0E0E0E;
          height: 45%;
          width: 2rem;

          border-radius: 30px 30px 0 0 ;
        }
      }
    }
  }

</style>
