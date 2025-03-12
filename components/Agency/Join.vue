<template>
  <section style="background-color: #041428;">
    <div class="container">
      <div class="row text-center text-white">
        <div class="col">
          <h2 class="display-5">
            Join Brieflly <br>
            Simplified Setup For Agencies
          </h2>
          <p>
            Only fully verified, top-tier agencies make the cut, so clients know they’re getting the best.
          </p>
        </div>
      </div>
      <div class="row">
        <div
          class="col-md-6 col-lg-4 mt-5"
          v-for="(feature, index) in features"
          :key="index"
        >
          <div
            class="card feature-card border-0 rounded-4 shadow-sm px-3 py-5 h-100 position-relative"
          >
            <div
              class="feature-card-icon position-absolute top-0 start-50 translate-middle rounded-circle border border-4 d-flex align-items-center justify-content-center"
              style="width: 50px; height: 50px; border-color: #041428 !important;"
            >
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

<script setup>
const features = [
  {
    title: 'Build Your Profile',
    description:
      'Sign up, complete your profile, and give us a glimpse into your agency’s experience and expertise. We want to know what makes you stand out.'
  },
  {
    title: 'Thorough Vetting',
    description:
      'Our team dives into your track record, reputation, and quality of work—only agencies that meet Brieflly’s standards for reliability and skill make it in.'
  },
  {
    title: 'Verified Reviews',
    description:
      'To strengthen your profile, we gather reviews directly from previous clients. We reach out for feedback to build a well-rounded, trustworthy profile for potential clients to see.'
  },
  {
    title: 'Welcome & Onboarding',
    description:
      'Once approved, we’ll walk you through the tools and guidelines, so you can jump right into briefs and projects with ease.'
  },
  {
    title: 'Matched Project Briefs',
    description:
      'With your profile polished and approved, you’ll start seeing project briefs that align with your agency’s expertise. Review and choose the projects that fit.'
  },
  {
    title: 'Milestone Payments, Right on Time',
    description:
      'Deliver quality work, hit your milestones, and count on secure, milestone-based payments at each step of the project.'
  }
]
</script>
