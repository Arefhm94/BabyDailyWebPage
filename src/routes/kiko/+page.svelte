<script lang="ts">
  import Hero from "$lib/components/site/Hero.svelte";
  import ScreenshotGallery from "$lib/components/site/ScreenshotGallery.svelte";
  import Features from "$lib/components/site/Features.svelte";
  import { Button } from "$lib/components/ui/button";
  import { CheckCircle2 } from "lucide-svelte";
  import heroImage from "$lib/assets/kiko_ss/home_dark.png";
  import smartCaptureImg from "$lib/assets/kiko_ss/smart_capture_light.png";
  import liveActivityImg from "$lib/assets/kiko_ss/live_activity_light.png";
  import widgetImg from "$lib/assets/kiko_ss/ios_widget_light.png";
  import partnerImg from "$lib/assets/kiko_ss/setting_parent_light.png";

  const APP_STORE_URL = "https://apps.apple.com/es/app/babydaily-tracker-routine/id6760598006?l=en-GB";
  const QR_CODE_URL = `https://api.qrserver.com/v1/create-qr-code/?data=${encodeURIComponent(APP_STORE_URL)}&size=200x200&margin=12&color=000000&bgcolor=ffffff&qzone=1&format=svg`;
</script>

<svelte:head>
  <title>Kiko – Baby Tracker | by OrdesaHub</title>
  <meta name="description" content="Kiko is a fast, beautiful baby tracker for iOS. Log feedings, diapers, and sleep right from your home screen. Sync instantly with your partner. Made by OrdesaHub." />
</svelte:head>

<Hero imageSrc={heroImage} />

<ScreenshotGallery />

<!-- ─── Feature Showcases ────────────────────────────────────────── -->
<section class="py-24 bg-background overflow-hidden relative">
  <div class="container mx-auto px-4 space-y-32">
    <!-- Showcase 1 -->
    <div class="flex flex-col lg:flex-row items-center gap-12 lg:gap-20">
      <div class="flex-1 space-y-6 max-w-xl">
        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-blue-500/10 text-blue-500 text-sm font-bold uppercase tracking-wider">
          AI Powered
        </div>
        <h2 class="text-4xl md:text-5xl font-extrabold tracking-tight">Log activities just by talking.</h2>
        <p class="text-lg text-muted-foreground leading-relaxed">
          Smart Capture uses precise on-device speech recognition to understand what you say. Just say "he drank 4 ounces and fell asleep", and Kiko logs both the feed and the nap instantly.
        </p>
        <ul class="space-y-3 pt-4">
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Hands-free voice transcription</span></li>
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Understands complex routines</span></li>
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>No personal data stored</span></li>
        </ul>
      </div>
      <div class="flex-1 right-tilt relative">
        <div class="absolute inset-0 bg-blue-500/20 blur-3xl rounded-full scale-110 -z-10"></div>
        <img src={smartCaptureImg} alt="Smart Capture" class="w-full max-w-sm mx-auto rounded-[2.5rem] border-[8px] border-slate-900 shadow-2xl" />
      </div>
    </div>

    <!-- Showcase 2 -->
    <div class="flex flex-col lg:flex-row-reverse items-center gap-12 lg:gap-20">
      <div class="flex-1 space-y-6 max-w-xl">
        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-orange-500/10 text-orange-500 text-sm font-bold uppercase tracking-wider">
          Stay in Sync
        </div>
        <h2 class="text-4xl md:text-5xl font-extrabold tracking-tight">Never lose track with Live Activities.</h2>
        <p class="text-lg text-muted-foreground leading-relaxed">
          Start a sleep or feeding timer and keep an eye on it directly from your Lock Screen. Check your baby's last activity directly on the Dynamic Island without unlocking your phone.
        </p>
        <ul class="space-y-3 pt-4">
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Persistent on Lock Screen</span></li>
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Dynamic Island support</span></li>
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>One-tap completion</span></li>
        </ul>
      </div>
      <div class="flex-1 left-tilt relative">
        <div class="absolute inset-0 bg-orange-500/20 blur-3xl rounded-full scale-110 -z-10"></div>
        <img src={liveActivityImg} alt="Live Activities" class="w-full max-w-sm mx-auto rounded-[2.5rem] border-[8px] border-slate-900 shadow-2xl" />
      </div>
    </div>

    <!-- Showcase 3 -->
    <div class="flex flex-col lg:flex-row items-center gap-12 lg:gap-20">
      <div class="flex-1 space-y-6 max-w-xl">
        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-green-500/10 text-green-500 text-sm font-bold uppercase tracking-wider">
          Always Accessible
        </div>
        <h2 class="text-4xl md:text-5xl font-extrabold tracking-tight">Interactive Home Screen Widgets.</h2>
        <p class="text-lg text-muted-foreground leading-relaxed">
          Log a diaper change or feed without ever opening the app. Kiko widgets display the latest activities right on your home screen so you and your partner always know what's happening.
        </p>
        <ul class="space-y-3 pt-4">
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>View recent logs at a glance</span></li>
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Interactive quick-logging</span></li>
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Real-time partner sync</span></li>
        </ul>
      </div>
      <div class="flex-1 right-tilt relative">
        <div class="absolute inset-0 bg-green-500/20 blur-3xl rounded-full scale-110 -z-10"></div>
        <img src={widgetImg} alt="Home Widgets" class="w-full max-w-sm mx-auto rounded-[2.5rem] border-[8px] border-slate-900 shadow-2xl" />
      </div>
    </div>

    <!-- Showcase 4 -->
    <div class="flex flex-col lg:flex-row-reverse items-center gap-12 lg:gap-20">
      <div class="flex-1 space-y-6 max-w-xl">
        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-purple-500/10 text-purple-500 text-sm font-bold uppercase tracking-wider">
          Partner Sharing
        </div>
        <h2 class="text-4xl md:text-5xl font-extrabold tracking-tight">Always in sync with your partner.</h2>
        <p class="text-lg text-muted-foreground leading-relaxed">
          Invite your partner or caregiver with a single tap. Every log — feedings, diapers, sleep — syncs in under a second across all devices so you're always on the same page, day or night.
        </p>
        <ul class="space-y-3 pt-4">
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Invite via email in one tap</span></li>
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Under-a-second real-time sync</span></li>
          <li class="flex items-center gap-3"><CheckCircle2 class="h-5 w-5 text-primary" /> <span>Private & secure — data stays yours</span></li>
        </ul>
      </div>
      <div class="flex-1 left-tilt relative">
        <div class="absolute inset-0 bg-purple-500/20 blur-3xl rounded-full scale-110 -z-10"></div>
        <img src={partnerImg} alt="Partner Sharing" class="w-full max-w-sm mx-auto rounded-[2.5rem] border-[8px] border-slate-900 shadow-2xl" />
      </div>
    </div>
  </div>
</section>

<style>
  .right-tilt { transform: perspective(1000px) rotateY(-8deg) rotateX(4deg); transition: transform 0.5s ease; }
  .right-tilt:hover { transform: perspective(1000px) rotateY(0deg) rotateX(0deg); }
  .left-tilt { transform: perspective(1000px) rotateY(8deg) rotateX(4deg); transition: transform 0.5s ease; }
  .left-tilt:hover { transform: perspective(1000px) rotateY(0deg) rotateX(0deg); }
</style>

<Features />


<!-- ─── Download / QR ──────────────────────────────────────────── -->
<section class="py-24 bg-primary text-primary-foreground">
  <div class="container mx-auto px-4 text-center space-y-10">
    <h2 class="text-4xl md:text-6xl font-extrabold tracking-tight">
      Ready to simplify parenting?
    </h2>
    <p class="text-primary-foreground/80 text-lg md:text-xl max-w-2xl mx-auto">
      Join parents using Kiko to stay in sync and give their babies the best care.
    </p>

    <!-- Download row -->
    <div class="flex flex-col sm:flex-row items-center justify-center gap-6">

      <!-- App Store badge -->
      <a
        href={APP_STORE_URL}
        target="_blank"
        rel="noopener noreferrer"
        id="cta-app-store-btn"
        class="inline-flex items-center gap-3 bg-white text-black rounded-2xl px-5 py-3 hover:opacity-85 transition-opacity active:scale-95 shadow-xl"
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 flex-shrink-0" viewBox="0 0 814 1000" fill="currentColor">
          <path d="M788.1 340.9c-5.8 4.5-108.2 62.2-108.2 190.5 0 148.4 130.3 200.9 134.2 202.2-.6 3.2-20.7 71.9-68.7 141.9-42.8 61.6-87.5 123.1-155.5 123.1s-85.5-39.5-164-39.5c-76 0-103.7 40.8-165.9 40.8s-105-57.8-155.5-127.4C46 405.6 0 280 0 160.4c0-112.1 55.1-171.2 128.3-171.2 71.9 0 97.6 36.1 154.3 36.1 56.7 0 90.1-40.8 162.3-40.8 62.2 0 115.5 33.1 149.4 84.4zm-215.4-187.7c30.7-36.5 52.2-87.5 52.2-138.5 0-7.1-.6-14.3-1.9-20.1-49.7 1.9-108.8 33.1-143.7 75.9-27.5 32.4-52.2 83.4-52.2 135.2 0 7.7 1.3 15.5 1.9 18.1 3.2.6 8.4 1.3 13.6 1.3 44.7 0 101.4-29.4 130.1-71.9z"/>
        </svg>
        <div class="flex flex-col leading-tight text-left">
          <span class="text-[10px] font-medium opacity-70">Download on the</span>
          <span class="text-lg font-bold tracking-tight">App Store</span>
        </div>
      </a>

      <Button
        href="mailto:arefsn89@gmail.com"
        size="lg"
        variant="outline"
        class="rounded-full px-10 h-14 text-base font-bold bg-transparent border-primary-foreground/30 text-primary-foreground hover:bg-primary-foreground hover:text-primary transition-all"
      >
        Get in touch
      </Button>
    </div>

    <!-- QR Code card -->
    <div class="flex flex-col items-center gap-4 pt-4">
      <p class="text-primary-foreground/60 text-sm tracking-wide uppercase font-medium">Or scan to download</p>
      <div class="qr-card bg-white rounded-3xl p-4 shadow-2xl inline-block">
        <img
          src={QR_CODE_URL}
          alt="QR code to download Kiko on the App Store"
          width="160"
          height="160"
          class="rounded-xl block"
        />
      </div>
      <p class="text-primary-foreground/40 text-xs">Point your camera at the code to open the App Store</p>
    </div>
  </div>
</section>
