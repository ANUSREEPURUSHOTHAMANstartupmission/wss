<script>
  import Splide from '@splidejs/splide';

  import {onMount, onDestroy} from 'svelte';

  export let splide = null;
  export let options = {};
  export let extensions = false;
  export let transition = false;

  let element;

  $: if (splide && options) {
    splide.options = options;
  }

  $: splide && splide.mount(extensions, transition);

  onMount(()=>{
    console.log(options);
    splide = new Splide(element, options);
    console.log(splide)
  });

  onDestroy(() => {
    splide && splide.destroy();
  });

</script>

<div class="splide" bind:this={element}>
	<div class="splide__track">
		<ul class="splide__list">
      <slot />
		</ul>
	</div>
</div>
