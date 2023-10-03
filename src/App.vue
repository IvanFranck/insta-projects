<template>
  <div class="container">
    <div class="card">
      <div class="card__image"></div>
      <div class="card__body">
        <h1>Improve your front-end skills by building projects</h1>
        <p>
          Scan the QR code to visit Frontend Mentor and take your coding skills to the next level
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">

.container{
  width: 100%;
  min-height: 100vh;
  display: grid;
  align-items: center;
  justify-items: center;
  padding: 20px;
}

.card{
  background-color: var(--color-white);
  border-radius: 20px;
  padding: 16px;
  display: flex;
  flex-direction: column;
  gap: 16px;

  &__image{
    background-image: url('./assets/images/image-qr-code.png');
    background-position: center;
    background-size: cover;
    height: 350px;
    width: 100%;
    border-radius: 12px;
  }

  &__body{
    text-align: center;

    h1{
      font-weight: 700;
      font-size: 25px;
      margin-bottom: 12px;
      color: var(--color-heading);
    }

    p{
      margin-bottom: 20px;
    }
  }
}
</style>