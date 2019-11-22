<template>
  <div class="container">
    <article class="helvetica">
      <header class="vh-100 bg-navy dt w-100 white">
        <div
          style="background:url(./bg.jpeg) no-repeat center right;background-size: cover;"
          class="dark-mask dtc v-mid cover ph3 ph4-m ph5-l"
        >
          <h1 class="f2 f-subheadline-l measure lh-title fw9 white">Welcome to self destructing chat</h1>
          <br />
          <register-user-input />
          <nuxt-link @click:native="{chatLinkClicked}">
            <div class="button">Create secure chat</div>
          </nuxt-link>
        </div>
      </header>
    </article>
  </div>
</template>

<script>
import RegisterUserInput from '~/components/registerUserInput'

export default {
  name: 'Home',
  components: { RegisterUserInput },
  methods: {
    chatLinkClicked() {
      const date = new Date()
      let hash = `jedkl1321_${Math.floor((date.getTime() * 3) / 2)}`
      this.$router.push({ name: 'chat', params: { id: hash } })
    }
  }
}
</script>

<style>
.button {
  width: 200px;
  border: 2px solid #fff;
  margin: 0 auto;
  padding: 20px;
  font-weight: bold;
  color: #fff;
}

a {
  text-decoration: none;
}

.button:hover {
  cursor: pointer;
}

.dark-mask {
  position: relative;
}

/* .dark-mask:after {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  content: '';
  background-color: #001b44;
  opacity: 0.4;
  top: 0;
  left: 0;
} */

.bg-navy {
  background-color: #001b44;
}

.white {
  color: #fff;
}

.cover {
  background-size: cover !important;
}

.bt {
  border-top-style: solid;
  border-top-width: 1px;
}

.b--black-10 {
  border-color: rgba(0, 0, 0, 0.1);
}

.cf:before,
.cf:after {
  content: ' ';
  display: table;
}

.cf:after {
  clear: both;
}

.cf {
  *zoom: 1;
}

.dn {
  display: none;
}

.db {
  display: block;
}

.dt {
  display: table;
}

.dtc {
  display: table-cell;
}

.fl {
  float: left;
  _display: inline;
}

.serif {
  font-family: georgia, times, serif;
}

.helvetica {
  font-family: 'helvetica neue', helvetica, sans-serif;
}

.fw6 {
  font-weight: 600;
}

.fw9 {
  font-weight: 900;
}

.vh-100 {
  height: 100vh;
}

.lh-title {
  line-height: 1.25;
}

.lh-copy {
  line-height: 1.5;
}

.mw6 {
  max-width: 32rem;
}

.w-50 {
  width: 50%;
}

.w-100 {
  width: 100%;
}

.black {
  color: #000;
}

.bg-light-pink {
  background-color: #ffa3d7;
}

.pl2 {
  padding-left: 0.5rem;
}

.pr1 {
  padding-right: 0.25rem;
}

.pb3 {
  padding-bottom: 1rem;
}

.pb5 {
  padding-bottom: 4rem;
}

.pv4 {
  padding-top: 2rem;
  padding-bottom: 2rem;
}

.ph3 {
  padding-left: 1rem;
  padding-right: 1rem;
}

.f2 {
  font-size: 2.25rem;
}

.f4 {
  font-size: 1.25rem;
}

.f5 {
  font-size: 1rem;
}

.f6 {
  font-size: 0.875rem;
}

.measure {
  max-width: 30em;
}

.center {
  margin-right: auto;
  margin-left: auto;
}

.v-mid {
  vertical-align: middle;
}

@media screen and (min-width: 30em) {
  .fw4-ns {
    font-weight: 400;
  }
}

@media screen and (min-width: 30em) and (max-width: 60em) {
  .ph4-m {
    padding-left: 2rem;
    padding-right: 2rem;
  }

  .f3-m {
    font-size: 1.5rem;
  }

  .f5-m {
    font-size: 1rem;
  }
}

@media screen and (min-width: 60em) {
  .dt-l {
    display: table;
  }

  .dtc-l {
    display: table-cell;
  }

  .w-50-l {
    width: 50%;
  }

  .pl0-l {
    padding-left: 0;
  }

  .pl2-l {
    padding-left: 0.5rem;
  }

  .pr0-l {
    padding-right: 0;
  }

  .pr2-l {
    padding-right: 0.5rem;
  }

  .pr3-l {
    padding-right: 1rem;
  }

  .pv4-l {
    padding-top: 2rem;
    padding-bottom: 2rem;
  }

  .ph5-l {
    padding-left: 4rem;
    padding-right: 4rem;
  }

  .f-subheadline-l {
    font-size: 5rem;
  }

  .f1-l {
    font-size: 3rem;
  }

  .f4-l {
    font-size: 1.25rem;
  }

  .measure-l {
    max-width: 30em;
  }
}
</style>
