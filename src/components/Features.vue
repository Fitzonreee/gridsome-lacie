<template>
    <section class="features">

      <div class="item item-1">
          <!-- <g-image class="item__image" alt="Capture" src="~/assets/images/CED_capture_lrg.jpg"/> -->
          <figure class="figure figure-1"></figure>
      </div>
      
      <div class="feature item item-2">
        <div class="feature__content">
          <h3 class="feature__headline">Capture</h3>
          <p class="feature__copy">Equipped with a RAID controller and 7200RPM drives, 12big boasts an impressive 2600MB/s data transfer speed making ingestion of 4/5/6K video a reality in a fraction of the time.</p>
          <ul class="feature__list">
            <li class="feature__item">
              <span class="key">Capacity</span>
              <span class="value">48TB / 72TB / 96TB</span>
            </li>
            <li class="feature__item">
              <span class="key">HDD daisy chain</span>
              <span class="value">up to six HDDs for 576TB</span>
            </li>
            <li class="feature__item">
              <span class="key">Ports</span>
              <span class="value">Dual Thunderbolt 3</span>
            </li>
          </ul>
        </div>
      </div>

      <div class="item item-3">
         <!-- <g-image class="item__image" alt="Capture" src="~/assets/images/CED_edit_lrg.jpg"/> -->
         <figure class="figure figure-3"></figure>
      </div>
      
      <div class="feature item item-4">
        <div class="feature__content">
          <h3 class="feature__headline">Edit</h3>
          <p class="feature__copy">Daisy chain up to two 4K displays or one 5K display for the ultimate editing workflow. Editing multiple streams of ProRes 422 (HQ), ProRes 444 XQ, as well as uncompressed HD 10-bit abd 12-bit video is a reality with 12big's focus on speed and capacity.</p>
          <ul class="feature__list">
            <li class="feature__item">
              <span class="key">Speed(s)</span>
              <span class="value">up to 2600MB/s</span>
            </li>
            <li class="feature__item">
              <span class="key">RAID 5 speed(s)</span>
              <span class="value">up to 1130MB/s</span>
            </li>
            <li class="feature__item">
              <span class="key">Display daisy chain</span>
              <span class="value">dual 4k or one 5k display</span>
            </li>
          </ul>
        </div>
      </div>
      

      
      <div class="item item-5">
         <!-- <g-image class="item__image" alt="Capture" fit="fill" src="~/assets/images/CED_deliver_lrg.jpg"/> -->
         <figure class="figure figure-5"></figure>
      </div>
      
      <div class="feature item item-6">  
        <div class="feature__content">
          <h3 class="feature__headline">Deliver</h3>
          <p class="feature__copy">Work faster, work smarter and consolidate all your files into a 96TB future-proof, RAID-protected solution. 12big has all the storage, speed and protection you need so you canfocus on delivering your best work.</p>
          <ul class="feature__list">
            <li class="feature__item">
              <span class="key">Interface transfer rates</span>
              <span class="value">Thunderbolt 3: 40Gb/s</span>
            </li>
            <li class="feature__item">
              <span class="key">RAID modes</span>
              <span class="value">0 / 1 / 5 / 6 / 10 / 50</span>
            </li>
            <li class="feature__item">
              <span class="key">USB-C cable power</span>
              <span class="value">45W (port A) or 15W (port B)</span>
            </li>
          </ul>
        </div>
      </div>

    </section>
</template>

<script>
export default {
  name: 'Features'
}
</script>

<style lang="scss" scoped>

.features {
  display: grid;

  @include medium {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: repeat(3, auto);
  }

  .item {
    background: $lightGray;
    display: flex;
    align-items: center;

    .figure {
        width: 100%;
        height: 100%;
        min-height: 300px;
        margin: 0;
        background-repeat: no-repeat;
        background-size: cover;
    }

    &-1 {
        .figure-1 {
            background-image: url(~@/assets/images/CED_capture_lrg.jpg);
        }
    }

    &-3 {
        .figure-3 {
            background-image: url(~@/assets/images/CED_edit_lrg.jpg);
        }
    }

    &-5 {
        .figure-5 {
            background-image: url(~@/assets/images/CED_deliver_lrg.jpg);
        }
    }

    

    &__image {
      object-fit: cover;
      width: 100%;
    }

    &-2,
    &-4,
    &-6 {
        padding: 0 2em;
    }

    &-2, 
    &-6 {                           
        @include medium {
            padding-left: 10%;
            padding-right: 20%;
        }
    }

    &-3 {
        @include medium {
            grid-column: 2 / span 1;
            grid-row: 2 / span 1;
        }
    }

    &-4 {
        @include medium {
            padding-left: 20%;
            padding-right: 10%;
            grid-column: 1 / span 1;
            grid-row: 2 / span 1;
        }
    }
  
  }
}

.feature {

  &__content {
    max-width: 46em;
    margin: 1em 0;
    padding: 1.25em 0 2em 0;
    color: $gray;
  }

  &__headline {
    text-transform: uppercase;
    color: $darkBlue;
    letter-spacing: 1px;
    font-size: 28px;
    margin: 0 0 0.5em 0;

    @include large {
        font-size: 48px;
    }

  }

  &__copy {
    font-size: 16px;
    margin-bottom: 2em;
    @include medium {
        font-size: 18px;
        margin-bottom: 3em;
    }
  }

  &__list {
    font-size: 12px;
    margin: 0;
    padding: 0;
    list-style-type: none;
  }

  &__item {
    padding: 0.85em 0;
    display: flex;
    border-top: 1px solid rgba($gray, 0.18);

    &:last-of-type {
      border-bottom: 1px solid rgba($gray, 0.18);;
    }

    .key, .value {
      // margin-right: auto;
      width: 50%;
    }
  }

}

</style>
