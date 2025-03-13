<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col-md-8 mx-auto" data-aos="fade-in">
          <div class="card border-0 bg-light rounded-5">
            <div class="card-body">
              <form @submit.prevent="handleSubmit" class="container mt-4">
                <!-- Name Field -->
                <div class="mb-4">
                  <label for="name" class="form-label">Full Name</label>
                  <div class="form-floating mb-3">
                    <input type="text" class="form-control form-control-lg rounded-pill" id="name"
                      placeholder="Enter your name" v-model="form.name" />
                    <label for="name" class="form-label">Enter your name</label>
                  </div>
                </div>

                <!-- Email Field -->
                <div class="mb-4">
                  <label for="email" class="form-label">Email</label>
                  <div class="form-floating mb-3">
                    <input type="email" class="form-control form-control-lg rounded-pill" id="email"
                      placeholder="Enter your email" v-model="form.email" />
                    <label for="email">Enter your email</label>
                  </div>
                </div>

                <!-- Company or Organization Field -->
                <div class="mb-4">
                  <label for="company" class="form-label">Company or Organization</label>
                  <div class="form-floating mb-3">
                    <input type="text" class="form-control form-control-lg rounded-pill" id="company"
                      placeholder="Enter your company name" v-model="form.company" />
                    <label for="company" class="form-label">Enter your company name</label>
                  </div>
                </div>

                <!-- Project Description Field -->
                <div class="mb-4">
                  <label for="project" class="form-label">Tell us about your project</label>
                  <div class="form-floating mb-3">
                    <textarea id="project" class="form-control form-control-lg rounded-5 h-100" rows="4"
                      placeholder="Share what you're working on and how Brieflly can help"
                      v-model="form.project"></textarea>
                    <label for="project">Share what you're working on and how Brieflly can
                      help</label>
                  </div>
                </div>

                <!-- Checkbox Options -->
                <div class="mb-4">
                  <label class="form-label">I am signing up as</label>
                  <div class="form-check mb-3">
                    <input type="checkbox" class="form-check-input" id="agency" value="Agency"
                      v-model="form.accountTypes" />
                    <label class="form-check-label" for="agency">An Agency</label> <br>
                    <small>Looking to offer services</small>
                  </div>
                  <div class="form-check">
                    <input type="checkbox" class="form-check-input" id="subscriber" value="Subscriber"
                      v-model="form.accountTypes" />
                    <label class="form-check-label" for="subscriber">A Business</label> <br>
                    <small>Looking to hire agencies</small>
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
