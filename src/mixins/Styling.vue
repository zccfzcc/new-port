<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

@Component
export default class Styling extends Vue {

  // LOCAL VARIABLES ------------------
   window: any = {
    width: 0,
    height: 0
  };

  // COMPUTED -------------------------
  // ---  TOP ---
  get nameFontSize() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return 'h4';
      case 'sm': return 'h3';
      case 'md': return 'h2';
      case 'lg': return 'h1';
      case 'xl': return 'h1';
      default: return 'h1';
    }
  }

  get cardDim() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return '60';
      case 'sm': return '60';
      case 'md': return '80';
      case 'lg': return '95';
      case 'xl': return '95';
      default: return '95';
    }
  }

  get newTopTop() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return (this.window.height / 2) - 200;
      case 'sm': return (this.window.height / 2) - 100;
      case 'md': return (this.window.height / 2) - 150;
      case 'lg': return (this.window.height / 2) - 200;
      case 'xl': return (this.window.height / 2) - 200;
      default: return this.window.height / 2;
    }
  }

  get newTopBottom() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return (this.window.height / 2) + 200;
      case 'sm': return (this.window.height / 2) + 100;
      case 'md': return (this.window.height / 2) + 150;
      case 'lg': return (this.window.height / 2) + 200;
      case 'xl': return (this.window.height / 2) + 200;
      default: return this.window.height / 2;
    }
  }

  // --- BOTTOM ---
  get projectsText() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return 'h4';
      case 'sm': return 'h3';
      case 'md': return 'h2';
      case 'lg': return 'h1';
      case 'xl': return 'h1';
      default: return 'h1';
    }
  }

  get cardWidth() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return '340';
      case 'sm': return '360';
      case 'md': return '360';
      case 'lg': return '400';
      case 'xl': return '400';
      default: return '360';
    }
  }

  get projectName() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return 'h5';
      case 'sm': return 'h4';
      case 'md': return 'h4';
      case 'lg': return 'h4';
      case 'xl': return 'h4';
      default: return 'h4';
    }
  }

  get projectText() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return 'body-1';
      case 'sm': return 'h6';
      case 'md': return 'body-1';
      case 'lg': return 'body-1';
      case 'xl': return 'body-1';
      default: return 'body-1';
    }
  }

  get projectTextWeight() {
    switch (this.$vuetify.breakpoint.name) {
      case 'xs': return 'normal';
      case 'sm': return 'light';
      case 'md': return 'normal';
      case 'lg': return 'normal';
      case 'xl': return 'normal';
      default: return 'normal';
    }
  }

  // LIFECYCLE EVENTS -----------------
  created() {
    window.addEventListener('resize', this.handleResize)
    this.handleResize();
  }

  destroyed() {
    window.removeEventListener('resize', this.handleResize)
  }

  // METHODS --------------------------
  handleResize() {
    this.window.width = window.innerWidth;
    this.window.height = window.innerHeight;
  }
}
</script>

<style>
.img {
  border-bottom: 1px solid #E0E0E0 !important;
}

</style>