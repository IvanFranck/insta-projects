<script setup>
</script>

<template>
  <div class="container">
    <div class="card">
      <div class="card-img"></div>
      <div class="card-content">
        <div class="card-title">
          <span>
            PERFUME
          </span>
          <h1>
            Gabrielle Essence <br/> Eau De Parfum
          </h1>
        </div>
        <div class="card-description">
          <p>
            A floral, solar and voluptuous ... CHANEL.
          </p>

          <div class="card-prices">
            <span class="actual">$14.79</span>
            <span class="old">$169,99</span>
          </div>
        </div>

        <div class="card-cta">
          <button>
            <div>
              <svg width="15" height="16" xmlns="http://www.w3.org/2000/svg"><path d="...." fill="#FFF"/></svg>
            </div>
            <span>Add to card</span>
          </button>
        </div>
      </div>
    
    </div>
    
  </div>
</template>


<style lang="scss" scoped>
.container{
  min-height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 12px;
}

.card{
  border: 1px solid var(--color-white);
  border-radius: 8px;
  background-color: var(--color-white);
  overflow: hidden;

  &-img{
    width: 100%;
    height: 300px;
    background-size: cover;
    background-position: center;
    background-image: url('./assets/image-product-mobile.jpg');
  }

  &-content{
    padding: 16px 12px;
  }
}

.card-title{

  span{
    font-family: var(--font-family-sans-serif-2);
    letter-spacing: 8px;
    font-size: 10px;
    font-weight: 300;
    margin-bottom: 8px;
  }

  h1{
    font-family: var(--font-family-serif);
    color: var(--color-heading);
    line-height: 36px;
    font-size: 32px;
    font-weight: 800;
  }
}

.card-description{

  margin-top: 16px;
  p{
    margin-bottom: 16px;
    
  }

  .card-prices{
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: start;
    align-items: center;
    gap: 12px;
    line-height: 36px;

    .actual{
      font-family: var(--font-family-serif);
      color: var(--color-primary);
      font-size: 32px;
      margin-bottom: 16px;
    }
    .old{
      text-decoration: line-through;
    }
  }
}

.card-cta{
  width: 100%;
  
  button{
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 8px;
    width: 100%;
    background-color: var(--color-primary);
    height: 40px;
    font-weight: 400;
    border-radius: 8px;
    border: none;
    offset: none;
    box-shadow: none;
    color: var(--color-white);
  }
}
</style>