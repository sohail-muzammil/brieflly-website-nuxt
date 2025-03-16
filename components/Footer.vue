<template>
  <footer style="background-color: #041428;" class="text-white">
    <section>
      <div class="container">
        <div class="row">
          <div class="col-md-3">
            <img src="~/assets/img/logo/logo.png" height="40" class="w-auto" alt="" />
            <p class="mt-4 pe-1">
              Grow your business to the next level. We connect you with the top expertise, so you only work with the
              best.
            </p>
          </div>
          <div class="col-sm-4 col-md-3 mt-4">
            <h2 class="lead fw-bold mb-4">Services</h2>
            <ul class="list-unstyled">
              <li class="pb-3">
                <NuxtLink class="link-light link-offset-2 link-underline-opacity-0 link-underline-opacity-100-hover"
                  to="/">Home</NuxtLink>
              </li>
              <li class="pb-3">
                <NuxtLink class="link-light link-offset-2 link-underline-opacity-0 link-underline-opacity-100-hover"
                  to="/about">About</NuxtLink>
              </li>
              <li class="pb-3">
                <NuxtLink class="link-light link-offset-2 link-underline-opacity-0 link-underline-opacity-100-hover"
                  to="/agency">For Agencies</NuxtLink>
              </li>
            </ul>
          </div>
          <div class="col-sm-4 col-md-3 mt-4">
            <h2 class="lead fw-bold mb-4">Information</h2>
            <ul class="list-unstyled">
              <li class="pb-3">
                <NuxtLink class="link-light link-offset-2 link-underline-opacity-0 link-underline-opacity-100-hover"
                  to="#">Blog</NuxtLink>
              </li>
              <li class="pb-3">
                <NuxtLink class="link-light link-offset-2 link-underline-opacity-0 link-underline-opacity-100-hover"
                  to="#">News</NuxtLink>
              </li>
            </ul>
          </div>
          <div class="col-sm-4 col-md-3 mt-4">
            <h2 class="lead fw-bold mb-4">Legal</h2>
            <ul class="list-unstyled">
              <li class="pb-3">
                <NuxtLink class="link-light link-offset-2 link-underline-opacity-0 link-underline-opacity-100-hover"
                  to="/legal/terms-of-service">Terms of Services</NuxtLink>
              </li>
              <li class="pb-3">
                <NuxtLink class="link-light link-offset-2 link-underline-opacity-0 link-underline-opacity-100-hover"
                  to="/legal/privacy-policy">Privacy Policy</NuxtLink>
              </li>
              <li class="pb-3">
                <NuxtLink class="link-light link-offset-2 link-underline-opacity-0 link-underline-opacity-100-hover"
                  to="/legal/cookie-policy">Cookie Policy</NuxtLink>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
    <div class="container">
      <hr>
    </div>
    <section>
      <div class="container">
        <div class="row">
          <div class="col-md-6">{{ new Date().getFullYear() }} Brieflly, All rights reserved</div>
          <div class="col-md-6 text-center text-md-end">
            <ul class="list-unstyled list-inline">
              <li class="list-inline-item">
                <a href="https://facebook.com/Brieflly" target="_blank">
                  <img src="~/assets/img/social/facebook.svg" alt="" width="30" height="30" />
                </a>
              </li>
              <li class="list-inline-item">
                <a href="https://www.instagram.com/brieflly" target="_blank">
                  <img src="~/assets/img/social/instagram.svg" alt="" width="30" height="30" />
                </a>
              </li>
              <li class="list-inline-item">
                <a href="https://www.linkedin.com/company/brieflly" target="_blank">
                  <img src="~/assets/img/social/linkedin.svg" alt="" width="30" height="30" />
                </a>
              </li>
              <!-- <li class="list-inline-item">
                <a href="#">
                  <img src="~/assets/img/social/youtube.svg" alt="" width="30" height="30" />
                </a>
              </li> -->
            </ul>
          </div>
        </div>
      </div>
    </section>
  </footer>
</template>
