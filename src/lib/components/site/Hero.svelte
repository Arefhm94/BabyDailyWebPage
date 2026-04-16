<script lang="ts">
  import { Button } from "$lib/components/ui/button";
  import { ArrowRight } from "lucide-svelte";

  const APP_STORE_URL = "https://apps.apple.com/es/app/babydaily-tracker-routine/id6760598006?l=en-GB";

  let { imageSrc = "" } = $props();
</script>

<section class="relative overflow-hidden pt-32 pb-24 lg:pt-40 lg:pb-32">
  <!-- Background blobs -->
  <div class="absolute inset-0 -z-10 bg-[radial-gradient(45%_40%_at_50%_40%,oklch(0.50_0.22_260/0.12)_0%,transparent_100%)]"></div>
  <div class="absolute top-0 left-1/2 -translate-x-1/2 -z-10 h-[600px] w-[600px] rounded-full bg-primary/8 blur-[120px]"></div>

  <div class="container mx-auto px-4">
    <div class="flex flex-col lg:flex-row items-center gap-12 lg:gap-20">

      <!-- Text block -->
      <div class="flex-1 text-center lg:text-left space-y-8 max-w-2xl">
        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-primary/10 text-primary text-xs font-bold uppercase tracking-wider animate-in fade-in slide-in-from-bottom-3 duration-700">
          <span>New</span>
          <span class="w-1 h-1 rounded-full bg-primary"></span>
          <span>By OrdesaHub</span>
        </div>

        <h1 class="text-5xl lg:text-7xl font-extrabold tracking-tight text-foreground leading-[1.1] animate-in fade-in slide-in-from-bottom-5 duration-700 delay-100">
          Track your baby's day,
          <span class="bg-clip-text text-transparent bg-gradient-to-r from-primary to-primary/50">
            effortlessly.
          </span>
        </h1>

        <p class="text-lg lg:text-xl text-muted-foreground leading-relaxed animate-in fade-in slide-in-from-bottom-7 duration-700 delay-200">
          A fast, beautiful baby tracker built for iOS. Log feedings, diapers, and sleep directly from your home screen, and sync instantly with your partner.
        </p>

        <!-- App Store badge -->
        <p class="text-xs text-muted-foreground/60 tracking-widest uppercase font-semibold animate-in fade-in duration-700 delay-400">Available on</p>

        <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-2 animate-in fade-in slide-in-from-bottom-9 duration-700 delay-300">
          <a
            href={APP_STORE_URL}
            target="_blank"
            rel="noopener noreferrer"
            class="inline-flex items-center gap-3 bg-foreground text-background rounded-2xl px-5 py-3 hover:opacity-80 transition-opacity active:scale-95 shadow-lg"
            id="hero-app-store-btn"
          >
            <!-- Apple logo -->
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 flex-shrink-0" viewBox="0 0 814 1000" fill="currentColor">
              <path d="M788.1 340.9c-5.8 4.5-108.2 62.2-108.2 190.5 0 148.4 130.3 200.9 134.2 202.2-.6 3.2-20.7 71.9-68.7 141.9-42.8 61.6-87.5 123.1-155.5 123.1s-85.5-39.5-164-39.5c-76 0-103.7 40.8-165.9 40.8s-105-57.8-155.5-127.4C46 405.6 0 280 0 160.4c0-112.1 55.1-171.2 128.3-171.2 71.9 0 97.6 36.1 154.3 36.1 56.7 0 90.1-40.8 162.3-40.8 62.2 0 115.5 33.1 149.4 84.4zm-215.4-187.7c30.7-36.5 52.2-87.5 52.2-138.5 0-7.1-.6-14.3-1.9-20.1-49.7 1.9-108.8 33.1-143.7 75.9-27.5 32.4-52.2 83.4-52.2 135.2 0 7.7 1.3 15.5 1.9 18.1 3.2.6 8.4 1.3 13.6 1.3 44.7 0 101.4-29.4 130.1-71.9z"/>
            </svg>
            <div class="flex flex-col leading-tight">
              <span class="text-[10px] font-medium opacity-80">Download on the</span>
              <span class="text-lg font-bold tracking-tight">App Store</span>
            </div>
          </a>
          <Button
            href="#features"
            variant="outline"
            size="lg"
            class="rounded-full px-8 h-14 text-base font-semibold transition-all active:scale-95"
          >
            See Features
            <ArrowRight class="ml-2 h-4 w-4" />
          </Button>
        </div>
      </div>

      <!-- Phone mockup -->
      <div class="flex-1 relative animate-in fade-in zoom-in-95 duration-700 delay-200">
        <div class="phone-tilt relative z-10 w-full max-w-[340px] mx-auto transition-all duration-700 ease-out">
          {#if imageSrc}
            <div class="relative rounded-[2.5rem] overflow-hidden border-[10px] border-slate-900 shadow-2xl bg-slate-900">
              <img
                src={imageSrc}
                alt="Kiko App"
                class="w-full h-auto block"
              />
              <div class="absolute inset-0 pointer-events-none bg-gradient-to-tr from-transparent via-white/5 to-white/10 opacity-20"></div>
            </div>
          {:else}
            <div class="aspect-[9/19.5] w-full bg-muted animate-pulse rounded-[3rem] shadow-2xl"></div>
          {/if}

          <!-- Glow blobs behind phone -->
          <div class="absolute -top-8 -right-8 w-28 h-28 bg-primary/20 rounded-full blur-3xl -z-10"></div>
          <div class="absolute -bottom-8 -left-8 w-28 h-28 bg-primary/30 rounded-full blur-3xl -z-10"></div>
        </div>
      </div>

    </div>
  </div>
</section>

<style>
  .phone-tilt {
    perspective: 1000px;
    transform: rotateY(-10deg) rotateX(5deg);
  }
  .phone-tilt:hover {
    transform: rotateY(0deg) rotateX(0deg);
  }
</style>
