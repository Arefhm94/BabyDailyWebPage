<script lang="ts">
  import './layout.css';
  import Header from '$lib/components/site/Header.svelte';
  import Footer from '$lib/components/site/Footer.svelte';

  let { children } = $props();
</script>

<svelte:head>
  <title>BabyDaily | Baby Tracker by OrdesaHub</title>
  <meta name="description" content="A fast, native baby tracker for iOS. Log feedings, diapers, and sleep right from your home screen. Proudly made by OrdesaHub." />
</svelte:head>

<div class="flex min-h-screen flex-col">
  <Header />
  <main class="flex-1">
    {@render children()}
  </main>
  <Footer />
</div>
