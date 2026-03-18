<script lang="ts">
  import ss1 from '$lib/assets/babydaily_ss/HomePageLight.png';
  import ss2 from '$lib/assets/babydaily_ss/InsightLight.png';
  import ss3 from '$lib/assets/babydaily_ss/ActivityTrendsLight.png';
  import ss4 from '$lib/assets/babydaily_ss/GrowthTracking.png';
  import ss5 from '$lib/assets/babydaily_ss/DailyPlanner.png';
  import ss6 from '$lib/assets/babydaily_ss/LiveActivity.png';
  import ss7 from '$lib/assets/babydaily_ss/PartnerSharing.png';
  import ss8 from '$lib/assets/babydaily_ss/SmartWidget.png';
  import ss9 from '$lib/assets/babydaily_ss/InsightDark.png';
  import ss10 from '$lib/assets/babydaily_ss/HomePageDark.png';

  const screenshots = [
    { src: ss1, label: 'Home Page' },
    { src: ss2, label: 'Insights' },
    { src: ss3, label: 'Activity Trends' },
    { src: ss4, label: 'Growth Tracking' },
    { src: ss5, label: 'Daily Planner' },
    { src: ss6, label: 'Live Activity' },
    { src: ss8, label: 'Smart Widget' },
    { src: ss7, label: 'Partner Sharing' },
    { src: ss9, label: 'Insights (Dark)' },
    { src: ss10, label: 'Home Page (Dark)' }
  ];
</script>

<section class="pt-32 pb-24 bg-[#f0ede8]">
  <div class="container mx-auto px-4 text-center mb-16 space-y-4">
    <h2 class="text-3xl md:text-5xl font-bold tracking-tight text-slate-900">App Interface</h2>
    <p class="text-slate-500 max-w-2xl mx-auto">Experience the beautiful and intuitive design of BabyDaily, crafted specifically for the modern parent.</p>
  </div>

  <div class="w-full flex flex-nowrap overflow-x-auto pt-12 pb-12 gap-10 snap-x no-scrollbar px-6 md:px-16 cursor-grab active:cursor-grabbing">
    {#each screenshots as screenshot}
      <div class="flex-none w-[260px] flex flex-col items-center gap-6 snap-start transition-transform hover:scale-105 duration-300">
        <div class="phone">
          <div class="screen">
            <img src={screenshot.src} alt={screenshot.label} />
          </div>
          <div class="dynamic-island"></div>
          <div class="glare"></div>
        </div>
        <span class="text-xs font-bold uppercase tracking-widest text-slate-400/80">{screenshot.label}</span>
      </div>
    {/each}
    <!-- End Spacer -->
    <div class="flex-none w-6 md:w-16 h-1"></div>
  </div>
</section>

<style>
  .no-scrollbar::-webkit-scrollbar {
    display: none;
  }
  .no-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }

  .phone {
    position: relative;
    width: 240px;
    height: 498px;
    border-radius: 50px;
    background: linear-gradient(160deg, #2c2c2e 0%, #1a1a1c 50%, #111113 100%);
    box-shadow:
      0 0 0 1px rgba(255, 255, 255, 0.1),
      0 0 0 2.5px #050507,
      0 0 0 4px rgba(255, 255, 255, 0.06),
      0 30px 80px rgba(0, 0, 0, 0.45),
      0 8px 24px rgba(0, 0, 0, 0.3),
      inset 0 1px 0 rgba(255, 255, 255, 0.12),
      inset 0 -1px 0 rgba(255, 255, 255, 0.03);
  }

  .phone::before {
    content: '';
    position: absolute;
    left: -4px;
    top: 108px;
    width: 3.5px;
    height: 30px;
    background: linear-gradient(180deg, #3a3a3c 0%, #222224 100%);
    border-radius: 2px 0 0 2px;
    box-shadow: 0 40px 0 #303032, 0 80px 0 #303032;
  }

  .phone::after {
    content: '';
    position: absolute;
    right: -4px;
    top: 138px;
    width: 3.5px;
    height: 56px;
    background: linear-gradient(180deg, #3a3a3c 0%, #222224 100%);
    border-radius: 0 2px 2px 0;
  }

  .screen {
    position: absolute;
    inset: 7px;
    border-radius: 44px;
    overflow: hidden;
    background: #000;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .screen img {
    width: calc(100% - 10px);
    height: calc(100% - 10px);
    object-fit: cover;
    object-position: top;
    display: block;
    border-radius: 38px;
  }

  .dynamic-island {
    position: absolute;
    top: 15px;
    left: 50%;
    transform: translateX(-50%);
    width: 82px;
    height: 26px;
    background: #000;
    border-radius: 20px;
    z-index: 10;
  }

  .glare {
    position: absolute;
    inset: 7px;
    border-radius: 44px;
    background: linear-gradient(135deg, rgba(255, 255, 255, 0.07) 0%, transparent 45%);
    pointer-events: none;
    z-index: 20;
  }
</style>
