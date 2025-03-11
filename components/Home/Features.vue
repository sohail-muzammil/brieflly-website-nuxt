<template>
  <section>
    <div class="container mb-5">
      <div class="row text-center mb-5">
        <div class="col">
          <h2 class="display-5">No More Wasted Time and Guesswork</h2>
        </div>
      </div>
      <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-4">
        <div v-for="(feature, index) in features" :key="index" class="col mt-5">
          <div class="card feature-card border-0 rounded-4 shadow-sm px-3 py-5 h-100 position-relative">
            <div class="feature-card-icon position-absolute top-0 start-50 translate-middle rounded-circle border border-4 border-white d-flex align-items-center justify-content-center"
              style="width: 50px; height: 50px;">
              {{ index + 1 }}
            </div>
            <div class="card-body mt-4">
              <h3 class="lead fw-bold">{{ feature.title }}</h3>
              <p>{{ feature.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          icon: 'bi-arrow-repeat',
          title: 'Get Clear, Actionable Briefs',
          description: 'Brieflly’s data-powered tool builds task lists, timelines, and cost estimates in minutes. Get everything you need upfront, without wasting time.'
        },
        {
          icon: 'bi-arrow-repeat',
          title: 'Stay in the Know, Stay on Track',
          description: 'Get real-time updates at every stage. Track progress, hit milestones, and keep your project moving on time, within scope, and with zero surprises.'
        },
        {
          icon: 'bi-arrow-repeat',
          title: 'Budget with Confidence',
          description: 'No more guessing games. You’ll know the costs upfront, and pay only for what’s done, keeping surprises out and your budget intact.'
        },
        {
          icon: 'bi-arrow-repeat',
          title: 'Own the Process, Streamline the Rest',
          description: 'No more juggling. Brieflly centralizes contracts, invoices, and communication, letting you handle everything in one platform. Less admin, more action.'
        },
        {
          icon: 'bi-arrow-repeat',
          title: 'Work with Experts You Can Trust',
          description: 'Brieflly instantly matches you with verified agencies who know how to deliver. No more guesswork, just the right talent for the job.'
        },
        {
          icon: 'bi-arrow-repeat',
          title: 'Pay Only For Results',
          description: 'Pay as your project advances. With Brieflly’s milestone-based payments, you’re always on budget and providers get rewarded when they deliver, keeping things moving without financial hiccups.'
        }
      ]
    }
  }
}
</script>

