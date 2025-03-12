<template>
    <section class="bg-light">
        <div class="container my-5">
            <div class="row text-center">
                <div class="col" data-aos="fade-in">
                    <h2 class="display-5">Hear it Straight from our early Users:</h2>
                </div>
            </div>
            <div class="row mt-5" data-aos="fade-in">
                <Carousel v-bind="carouselOptions">
                    <Slide v-for="(testimonial, index) in testimonials" :key="index">
                        <div class="card border-0 rounded-5 p-4 h-100">
                            <div class="quotes display-5 text-body-tertiary">
                                <i class="bi bi-quote"></i>
                            </div>
                            <div class="card-body">
                                <p class="fw-bold">{{ testimonial.title }}</p>
                                <p class="card-text">{{ testimonial.description }}</p>
                                <div class="d-flex align-items-center pt-2">
                                    <!-- <img :src="testimonial.image" alt="testimonial image"> -->
                                    <div>
                                        <h5 class="card-title fw-bold">{{ testimonial.name }}</h5>
                                        <span class="text-secondary">{{ testimonial.company }}</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </Slide>
                    <template #addons>
                        <Pagination />
                        <Navigation />
                    </template>
                </Carousel>
            </div>
        </div>
    </section>
</template>

<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

export default {
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation
    },
    data() {
        return {
            carouselOptions: {
                autoplay: 4000,
                loop: true,
                mouseDrag: true,
                itemsToScroll: 1,
                snapAlign: 'center',
                wrapAround: false,
                gap: 5,
                breakpointMode: 'carousel',
                breakpoints: {
                    500: {
                        itemsToShow: 1,
                        snapAlign: 'center',
                    },
                    700: {
                        itemsToShow: 2,
                        snapAlign: 'start',
                    },
                },
            },
            testimonials: [
                {
                    title: 'Cut Project Planning Time by 75% with Seamless Brief Creation',
                    description:
                        '"Brieflly took the hassle out of finding the right agency. In just minutes, we had a structured brief and were matched with a team that understood our vision. What would have taken weeks to set up was done in a day! We launched faster and saved time we could reinvest into growing our business."',
                    image: 'https://codingyaar.com/wp-content/uploads/square-headshot-1.png',
                    name: 'Michael Tan',
                    company: 'COO, ScaleUp Solutions',
                },
                {
                    title: 'Doubled Our ROI with a Perfectly Matched Marketing Partner',
                    description:
                        '"Finding an agency that truly aligned with our needs used to be a challenge. With Brieflly, we were connected to a marketing team that not only met but exceeded our expectations. Our ad performance improved, and we saw a 2X return on investment in just three months!"',
                    image: 'https://codingyaar.com/wp-content/uploads/square-headshot-2.png',
                    name: 'Sophia Liew',
                    company: 'Head of Growth, NextGen Tech',
                },
                {
                    title: '60% Faster Web Development with Expertly Vetted Agencies',
                    description:
                        '"Brieflly transformed how we approach project outsourcing. Instead of sifting through endless agency lists, we filled out a brief, got matched instantly, and had our project kicked off in record time. The results? A fully developed platform delivered 60% faster than expected!"',
                    image: 'https://codingyaar.com/wp-content/uploads/bootstrap-profile-card-image.jpg',
                    name: 'David Chua',
                    company: 'CTO, Finovate Solutions',
                },
                {
                    title: 'Scaling Internationally Without the Hiring Headache',
                    description:
                        '"Expanding into new markets required local expertise, but hiring in-house wasn’t feasible. Brieflly connected us with a multilingual digital agency that handled everything—from content localization to ad campaigns. We successfully launched in three new regions without adding to our overhead."',
                    image: 'https://codingyaar.com/wp-content/uploads/square-headshot-2.png',
                    name: 'Isabelle Renaud',
                    company: 'VP of Marketing, GlobalRetail',
                },
                {
                    title: 'Reduced Project Costs by 30% with Transparent Pricing',
                    description:
                        '"We’ve worked with agencies before, but pricing was always a guessing game. Brieflly’s transparent model gave us clarity upfront, ensuring we stayed within budget. Not only did we cut costs by 30%, but we also gained a long-term partner for future projects."',
                    image: 'https://codingyaar.com/wp-content/uploads/bootstrap-profile-card-image.jpg',
                    name: 'Jason Wong',
                    company: 'Founder, Evolve DTC',
                },
            ],
        }
    },
}
</script>
