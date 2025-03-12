<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col-md-8 mx-auto">
          <div class="card border-0 bg-light rounded-5">
            <div class="card-body">
              <form @submit.prevent="handleSubmit" class="container mt-4">
            <!-- Name Field -->
            <div class="mb-3">
              <label for="name" class="form-label">Full Name</label>
              <input type="text" class="form-control" id="name" placeholder="Enter your name" v-model="form.name" />
            </div>

            <!-- Email Field -->
            <div class="mb-3">
              <label for="email" class="form-label">Email</label>
              <input type="email" class="form-control" id="email" placeholder="Enter your email" v-model="form.email" />
            </div>

            <!-- Company or Organization Field -->
            <div class="mb-3">
              <label for="company" class="form-label">Company or Organization</label>
              <input type="text" class="form-control" id="company" placeholder="Enter your company name"
                v-model="form.company" />
            </div>

            <!-- Project Description Field -->
            <div class="mb-3">
              <label for="project" class="form-label">Tell us about your project</label>
              <textarea id="project" class="form-control"
                placeholder="Share what you're working on and how Brieflly can help" v-model="form.project"></textarea>
            </div>

            <!-- Checkbox Options -->
            <div class="mb-3">
              <label class="form-label">I am signing up as</label>
              <div class="form-check">
                <input type="checkbox" class="form-check-input" id="agency" value="Agency"
                  v-model="form.accountTypes" />
                <label class="form-check-label" for="agency">An Agency</label>
              </div>
              <div class="form-check">
                <input type="checkbox" class="form-check-input" id="subscriber" value="Subscriber"
                  v-model="form.accountTypes" />
                <label class="form-check-label" for="subscriber">A Business</label>
              </div>
            </div>

            <!-- Submit Button -->
            <button type="submit" class="btn btn-primary rounded-pill mt-4">Submit</button>
          </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  company: '',
  project: '',
  accountTypes: []
})

function handleSubmit() {
  // Handle form submission (e.g., send data to an API)
  console.log('Form Submitted:', form.value)
}
</script>
