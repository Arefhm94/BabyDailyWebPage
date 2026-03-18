<script lang="ts">
  import { Shield, Lock, Trash2, Mail } from "lucide-svelte";
</script>

<svelte:head>
  <title>Privacy Policy | BabyDaily</title>
  <meta name="description" content="BabyDaily Privacy Policy. Learn about our data collection, security, and privacy practices." />
</svelte:head>

<section class="py-16 md:py-24 bg-slate-50 dark:bg-slate-950">
  <div class="container mx-auto px-4 max-w-4xl">
    <div class="space-y-4 mb-12">
      <h1 class="text-4xl md:text-5xl font-extrabold tracking-tight">Privacy Policy</h1>
      <p class="text-muted-foreground italic">Last Updated: March 16, 2026</p>
    </div>

    <div class="space-y-12 bg-background border rounded-3xl p-8 md:p-12 shadow-sm">
      <div class="p-6 rounded-2xl bg-primary/5 border border-primary/10 flex gap-4 items-start">
        <Shield class="h-6 w-6 text-primary shrink-0 mt-1" />
        <p class="text-sm leading-relaxed">
          This Privacy Policy explains how BabyDaily ("we," "our," or "us") collects, uses, securely stores, and
          protects your information. We are committed to upholding the highest standards of privacy and fully comply
          with the Apple App Store Guidelines, Google Play Data Safety requirements, the General Data Protection
          Regulation (GDPR), and the California Consumer Privacy Act (CCPA).
        </p>
      </div>

      <section class="space-y-4">
        <h2 class="text-2xl font-bold border-b pb-2">1. Information We Collect</h2>
        <p class="text-muted-foreground leading-relaxed">
          We only collect the absolute minimum information necessary to provide the core functionality of BabyDaily
          (tracking and syncing baby care events).
        </p>
        <ul class="space-y-4 list-disc pl-6 text-muted-foreground">
          <li><strong>Account Information:</strong> When you register using a third-party Single Sign-On provider (Sign In
            with Apple, Google Sign-In), we receive and store your basic identifier, such as your email address and name.
          </li>
          <li><strong>Baby Profile Data:</strong> To personalize the experience, you manually provide information about
            your child (such as their first name, gender, and date of birth).</li>
          <li><strong>User-Generated Content (Health & Activity Logs):</strong> You actively input the core data of the
            app, including sleep timers, feeding logs, diaper changes, and custom events. This includes timestamps and
            optional notes you attach to logs.</li>
        <li><strong>Device and Usage Analytics:</strong> We collect anonymous, aggregated crash reports and basic usage
          metrics (such as App version and OS version) to identify bugs and improve the app. This data is not linked to
          your identity or baby profiles.</li>
        </ul>
      </section>

      <section class="space-y-4">
        <h2 class="text-2xl font-bold border-b pb-2">2. How We Use Your Information</h2>
        <p class="text-muted-foreground">Your data is used exclusively to operate, maintain, and provide the features of BabyDaily:</p>
        <ul class="space-y-4 list-disc pl-6 text-muted-foreground">
          <li><strong>Syncing and Backup:</strong> To securely sync your logged activities across your own devices and
            with partners or caregivers you explicitly invite to your baby's profile.</li>
          <li><strong>Analytics & Predictions:</strong> To analyze the data locally on your device or via secure cloud
            functions to provide you with daily summaries, sleep trends, and predictive insights (e.g., predicted next
            nap).</li>
          <li><strong>Customer Support:</strong> To assist you with account-related inquiries or technical issues.</li>
        </ul>
      </section>

      <section class="space-y-4">
        <h2 class="text-2xl font-bold border-b pb-2 flex items-center gap-2">
          <Lock class="h-5 w-5 text-primary" />
          3. Data Storage, Security, and Protection
        </h2>
        <p class="text-muted-foreground">
          We take the security of your family's data very seriously. BabyDaily relies on enterprise-grade infrastructure
          to protect your information:
        </p>
        <ul class="space-y-4 list-disc pl-6 text-muted-foreground">
          <li><strong>Secure Hosting:</strong> Your data is hosted by Supabase, a highly secure and compliant database
            infrastructure provider.</li>
          <li><strong>Encryption in Transit and at Rest:</strong> All data transmitted between the App and our servers is
            encrypted using standard HTTPS/TLS protocols. Data stored in the database is encrypted at rest.</li>
          <li><strong>Row Level Security (RLS):</strong> We employ strict, database-level Row Level Security policies.
            This means that a baby's profile data can <strong>only</strong> be queried, read, or modified by the user who
            created it, or by a specific user who has actively accepted an invitation to share that profile.</li>
        </ul>
      </section>

      <section class="space-y-4">
        <h2 class="text-2xl font-bold border-b pb-2">4. Third-Party Sharing and Disclosure</h2>
        <p class="font-semibold">We do not, and will never, sell your personal data or your baby's data to advertisers, data brokers, or
          any other third parties.</p>
        <p class="text-muted-foreground">We share limited data strictly with trusted service providers necessary to run the application:</p>
        <ul class="space-y-4 list-disc pl-6 text-muted-foreground">
          <li><strong>Authentication Providers:</strong> Apple (Sign In with Apple) and Google (Google Sign-In) to verify
            your identity.</li>
          <li><strong>Hosting & Database:</strong> Supabase (provides our database and real-time syncing infrastructure).
          </li>
          <li><strong>Payment Processing:</strong> RevenueCat, Apple App Store, and Google Play Store process all in-app
            subscriptions.</li>
        </ul>
      </section>

      <section class="space-y-4">
        <h2 class="text-2xl font-bold border-b pb-2 flex items-center gap-2">
          <Trash2 class="h-5 w-5 text-destructive" />
          6. Data Retention and Account Deletion
        </h2>
        <p class="text-muted-foreground">You own your data and maintain total control over it.</p>
        <ul class="space-y-4 list-disc pl-6 text-muted-foreground">
          <li><strong>Data Retention:</strong> We keep your data only as long as your account remains active.</li>
          <li><strong>Log Deletion:</strong> You can delete any individual log or event directly from within the app at
            any time.</li>
          <li><strong>Full Account Deletion:</strong> You have the right to request the complete erasure of your account
            and all associated data. You can perform this action entirely within the App by navigating to <strong>Settings
            &gt; Delete Account</strong>.</li>
        </ul>
      </section>

      <section class="space-y-4 pt-8 border-t">
        <h2 class="text-2xl font-bold">9. Contact Us</h2>
        <p class="text-muted-foreground">
          If you have any questions, concerns, or requests regarding this Privacy Policy or your data, please contact our
          Data Protection Officer at:
        </p>
        <div class="flex items-center gap-2 p-4 rounded-xl bg-muted/50 w-fit">
          <Mail class="h-5 w-5 text-primary" />
          <span class="font-mono font-semibold">arefsn89@gmail.com</span>
        </div>
      </section>
    </div>
  </div>
</section>
