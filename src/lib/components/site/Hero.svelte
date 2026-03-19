<script lang="ts">
  import { Button } from "$lib/components/ui/button";
  import { Apple, Play, ArrowRight } from "lucide-svelte";
  
  let { imageSrc = "" } = $props();
</script>

<section class="relative overflow-hidden pt-32 pb-24 lg:pt-40 lg:pb-32">
  <!-- Dynamic Background Gradient -->
  <div class="absolute inset-0 -z-10 bg-[radial-gradient(45%_40%_at_50%_40%,var(--color-primary-foreground)_0%,transparent_100%)] opacity-20"></div>
  <div class="absolute top-0 left-1/2 -translate-x-1/2 -z-10 h-[600px] w-[600px] rounded-full bg-primary/10 blur-[120px]"></div>

  <div class="container mx-auto px-4">
    <div class="flex flex-col lg:flex-row items-center gap-12 lg:gap-20">
      <div class="flex-1 text-center lg:text-left space-y-8 max-w-2xl">
        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-primary/10 text-primary text-xs font-bold uppercase tracking-wider animate-in fade-in slide-in-from-bottom-3 duration-1000">
          <span>New</span>
          <span class="w-1 h-1 rounded-full bg-primary"></span>
          <span>By OrdesaHub</span>
        </div>
        
        <h1 class="text-5xl lg:text-7xl font-extrabold tracking-tight text-foreground leading-[1.1] animate-in fade-in slide-in-from-bottom-5 duration-1000 delay-200">
          Track your baby's day, <span class="bg-clip-text text-transparent bg-gradient-to-r from-primary to-primary/60">effortlessly.</span>
        </h1>
        
        <p class="text-lg lg:text-xl text-muted-foreground leading-relaxed animate-in fade-in slide-in-from-bottom-7 duration-1000 delay-300">
          A fast, native baby tracker built for iOS. Log feedings, diapers, and sleep directly from your home screen, and sync instantly with your partner.
        </p>
        
        <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-4 animate-in fade-in slide-in-from-bottom-10 duration-1000 delay-500">
          <Button size="lg" class="rounded-full px-8 h-14 text-base font-semibold shadow-lg shadow-primary/20 hover:shadow-primary/40 transition-all active:scale-95">
            Get for iOS
            <ArrowRight class="ml-2 h-4 w-4" />
          </Button>
          <Button variant="outline" size="lg" class="rounded-full px-8 h-14 text-base font-semibold hover:bg-muted/50 transition-all active:scale-95">
            Learn More
          </Button>
        </div>
      </div>
      
      <div class="flex-1 relative animate-in fade-in zoom-in duration-1000 delay-300">
        <div class="relative z-10 w-full max-w-[380px] mx-auto perspective-1000 rotate-y-[-10deg] rotate-x-[5deg] hover:rotate-0 transition-all duration-700 ease-out">
          {#if imageSrc}
            <div class="relative rounded-[2.5rem] overflow-hidden border-[12px] border-slate-900 shadow-2xl bg-slate-900">
              <img 
                src={imageSrc} 
                alt="BabyDaily App Mockup" 
                class="w-full h-auto block"
              />
              <!-- Vignette / Dark Edges Overlay (Reduced intensity) -->
              <div class="absolute inset-0 pointer-events-none shadow-[inset_0_0_20px_rgba(0,0,0,0.15),inset_0_0_60px_rgba(0,0,0,0.1)]"></div>
              <!-- Subtle Gloss Reflection (Reduced opacity) -->
              <div class="absolute inset-0 pointer-events-none bg-gradient-to-tr from-transparent via-white/5 to-white/10 opacity-20"></div>
            </div>
          {:else}
            <div class="aspect-[9/19.5] w-full bg-muted animate-pulse rounded-[3rem] shadow-2xl"></div>
          {/if}
          
          <!-- Decorative elements -->
          <div class="absolute -top-10 -right-10 w-32 h-32 bg-primary/20 rounded-full blur-3xl"></div>
          <div class="absolute -bottom-10 -left-10 w-32 h-32 bg-primary/30 rounded-full blur-3xl"></div>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .perspective-1000 {
    perspective: 1000px;
  }
  .rotate-y-\[-10deg\] {
    transform: rotateY(-10deg);
  }
  .rotate-x-\[5deg\] {
    transform: rotateX(5deg);
  }
</style>
