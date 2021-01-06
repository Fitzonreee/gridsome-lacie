<template>
    <section class="hero container">
      <g-image class="hero__image" alt="LaCie hero image" src="~/assets/images/12big_header_lrg.png"/>
      
      <div class="hero__content">
        
        <div class="hero__slider">
          <g-image v-if="show" :class="{active: show}" class="image" alt="LaCie Big12" src="~/assets/images/LaCie_12big_right_be.jpg"/>
          <g-image v-if="!show" class="image" alt="LaCie Big12" src="~/assets/images/LaCie_12big_right_be_exp.jpg"/>
          <ul class="dots">
            <li v-on:click="show = true" class="dot" :class="{active: show}"></li>
            <li v-on:click="show = false" class="dot" :class="{active: !show}"></li>
          </ul>
        </div>
        
        <div class="hero__headline">
          <h1 class="headline">Made for big ideas.</h1>
        </div>
        
        <div class="hero__copy-wrapper">
          <h2 class="hero__sub-headline">Introducing the world's largest desktop DAS drive.<br class="large"> The new LaCie 12big Thunderbolt 3 <span class="text-dark">| 96TB</span></h2>
          <p class="hero__copy">The new LaCie 12big Thunderbolt 3 has all the capacity and speed to make your biggest ideas come to life.</p>
          <a href="#" class="hero__cta">Learn more</a>
        </div>

      </div>
    </section>
</template>

<script>
export default {
  name: 'Hero',
  data() {
    return {
      show: true,
    }
  }
}
</script>

<style lang="scss" scoped>

.hero {

  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  &__image {
    max-width: 130%;
    display: block;

    @include medium {
      max-width: 972px;
    }
    
  }

  &__content {
    display: grid;
    grid-template-columns: 150px auto;
    grid-template-rows: repeat(2, minmax(min-content, auto));
    padding: 2em;
    margin: 0 auto;

    @include medium {
      grid-template-columns: 250px auto;
    }
  }

  &__slider,
  &__headline,
  &__copy-wrapper {
    display: flex;
  }

  &__slider {
    grid-column: 1 / span 1;
    grid-row: 1 / span 1;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    .image {
      max-width: 100px;
      @include medium {
        max-width: 100%;
      }
    }

    @include medium {
      grid-row: 1 / span 2;
    }
  }

  &__headline {
    align-items: flex-end;
    grid-column: 2 / span 1;
    grid-row: 1 / span 1;
    font-size: 24px;
    padding-bottom: 1em;
    color: $darkBlue;

    @include medium {
      font-size: 30px;
      padding-bottom: 0em;
    }

    .headline {
      margin: 0;
    }

  }

  &__copy-wrapper {
    grid-column: 1 / span 2;
    grid-row: 2 / span 1;
    flex-direction: column;
    align-items: flex-start;
    
    @include medium {
      grid-column: 2 / span 1;
      grid-row: 2 / span 1;
    }
  }

  &__sub-headline {
    font-size: 18px;
    color: $lightBlue;
    margin: 0;
    padding-top: 0.5em;

    @include medium {
      font-size: 26px;
    }

    .text-dark {
      color: $darkBlue;
    }

  }

  &__copy {
    color: $gray;
    font-size: 16px;
    max-width: 80%;
  }

  &__cta {
    background: $darkBlue;
    color: $white;
    text-decoration: none;
    text-transform: uppercase;
    padding: 0.5em 2em;
    margin-top: 1em;
    letter-spacing: 1px;
  }

  .dots {
    list-style-type: none;
    padding: 0;
    display: none;

    @include medium {
      display: flex;
      flex-direction: row;
      margin: 1em 0 0 0;
    }

  }

  .dot {
    width: 18px;
    height: 18px;
    border-radius: 100%;
    background: $lightGray;
    margin: 0 0.5em;

    &.active {
      background: $lightBlue;
    }

    &:hover {
      cursor: pointer;
    }
  }

}

</style>
