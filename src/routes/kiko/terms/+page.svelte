<script lang="ts">
  import { FileText, ExternalLink, Mail } from "lucide-svelte";
</script>

<svelte:head>
  <title>Terms of Use | Kiko – Baby Tracker</title>
  <meta name="description" content="Kiko – Baby Tracker Terms of Use." />
</svelte:head>

<section class="py-16 md:py-24 bg-background">
  <div class="container mx-auto px-4 max-w-4xl">
    <div class="space-y-4 mb-12">
      <h1 class="text-4xl md:text-5xl font-extrabold tracking-tight">Terms of Use (EULA)</h1>
      <p class="text-muted-foreground italic">Last Updated: April 7, 2026</p>
    </div>

    <div class="space-y-8 bg-background border rounded-3xl p-8 md:p-12 shadow-sm">

      <div class="p-6 rounded-2xl bg-primary/5 border border-primary/10 flex gap-4 items-start">
        <FileText class="h-6 w-6 text-primary shrink-0 mt-1" />
        <p class="text-sm leading-relaxed">
          Kiko – Baby Tracker ("the App") applies the standard Apple Licensed Application End User License Agreement (EULA).
        </p>
      </div>

      <section class="space-y-4 text-center py-12">
        <p class="text-muted-foreground text-lg mb-8 max-w-2xl mx-auto">
          By downloading, installing, or using the App, you agree to be bound by the standard Apple Terms of Use (EULA).
        </p>
        
        <a 
          href="https://www.apple.com/legal/internet-services/itunes/dev/stdeula/" 
          target="_blank"
          rel="noopener noreferrer"
          class="inline-flex items-center justify-center gap-2 bg-primary text-primary-foreground hover:bg-primary/90 h-12 px-8 rounded-full font-semibold transition-colors"
        >
          View Standard Apple EULA
          <ExternalLink class="h-4 w-4" />
        </a>
      </section>

      <!-- Contact -->
      <section class="space-y-4 pt-8 border-t">
        <h2 class="text-2xl font-bold">Contact Us</h2>
        <p class="text-muted-foreground">If you have any questions, please contact us:</p>
        <div class="flex items-center gap-2 p-4 rounded-xl bg-muted/50 w-fit">
          <Mail class="h-5 w-5 text-primary" />
          <a href="mailto:arefsn89@gmail.com" class="font-mono font-semibold hover:text-primary transition-colors">arefsn89@gmail.com</a>
        </div>
        <p class="text-sm text-muted-foreground">OrdesaHub · arefsn89@gmail.com</p>
      </section>

    </div>
  </div>
</section>
