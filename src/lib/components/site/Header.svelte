<script lang="ts">
  import { Button } from "$lib/components/ui/button";
  import { Baby, Activity } from "lucide-svelte";
</script>

<header class="sticky top-0 z-50 w-full border-b bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60">
  <div class="container flex h-16 items-center justify-between mx-auto px-4">
    <div class="flex items-center gap-8">
      <a href="/" class="flex items-center space-x-2 group">
        <div class="bg-foreground p-1 rounded-lg transition-transform group-hover:scale-110">
          <Activity class="h-5 w-5 text-background" />
        </div>
        <span class="inline-block font-extrabold text-xl tracking-tighter">OdesaHub</span>
      </a>
      
      <nav class="hidden md:flex items-center space-x-8 text-sm font-medium">
        <a href="/babydaily" class="flex items-center gap-2 transition-colors hover:text-primary text-muted-foreground">
          <Baby class="h-4 w-4" />
          <span>BabyDaily</span>
        </a>
        <a href="/#about" class="transition-colors hover:text-primary text-muted-foreground">About</a>
        <a href="/#portfolio" class="transition-colors hover:text-primary text-muted-foreground">Portfolio</a>
      </nav>
    </div>
    
    <div class="flex items-center gap-4">
      <Button variant="default" class="rounded-full px-6 bg-primary text-primary-foreground">Get App</Button>
    </div>
  </div>
</header>
