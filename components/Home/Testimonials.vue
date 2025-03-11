<template>
    <section class="bg-light">
        <div class="container my-5">
            <div class="row text-center">
                <div class="col">
                    <h2 class="display-5">Hear it Straight from our early Users:</h2>
                </div>
            </div>
            <div class="row mt-5">
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
                                    <img :src="testimonial.image" alt="testimonial image">
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
                    title: 'Cut Website Redesign Time by 50% and Came in 20% Under Budget',
                    description:
                        '"We were struggling to find a reliable agency for our website redesign, and the manual vetting process was taking far too long. That’s when we turned to Brieflly. In less than 10 minutes, their brief creation tool helped us generate a clear, detailed project scope, complete with tasks and budget estimates. Brieflly then matched us with a pre-vetted creative agency that fit our exact needs. Thanks to Brieflly, we launched the project 50% faster than expected and, thanks to the platform’s transparent pricing, we even came in 20% under budget. Brieflly has completely transformed the way we handle projects."',
                    image: 'https://codingyaar.com/wp-content/uploads/square-headshot-1.png',
                    name: 'Jane Doe',
                    company: 'CEO, Example Company',
                },
                {
                    title: '30% Increase in Lead Generation with the Right Marketing Team',
                    description:
                        '"We were struggling to find a reliable agency for our website redesign, and the manual vetting process was taking far too long. That’s when we turned to Brieflly. In less than 10 minutes, their brief creation tool helped us generate a clear, detailed project scope, complete with tasks and budget estimates. Brieflly then matched us with a pre-vetted creative agency that fit our exact needs. Thanks to Brieflly, we launched the project 50% faster than expected and, thanks to the platform’s transparent pricing, we even came in 20% under budget. Brieflly has completely transformed the way we handle projects."',
                    image: 'https://codingyaar.com/wp-content/uploads/square-headshot-2.png',
                    name: 'June Doe',
                    company: 'CEO, Example Company',
                },
                {
                    title: 'New Website design Time by 90% and Came in 10% Under Budget',
                    description:
                        '"We were struggling to find a reliable agency for our website redesign, and the manual vetting process was taking far too long. That’s when we turned to Brieflly. In less than 10 minutes, their brief creation tool helped us generate a clear, detailed project scope, complete with tasks and budget estimates. Brieflly then matched us with a pre-vetted creative agency that fit our exact needs. Thanks to Brieflly, we launched the project 50% faster than expected and, thanks to the platform’s transparent pricing, we even came in 20% under budget. Brieflly has completely transformed the way we handle projects"',
                    image: 'https://codingyaar.com/wp-content/uploads/bootstrap-profile-card-image.jpg',
                    name: 'John Doe',
                    company: 'CEO, Example Company',
                },
                {
                    title: '30% Increase in Lead Generation with the Right Marketing Team',
                    description:
                        '"We were struggling to find a reliable agency for our website redesign, and the manual vetting process was taking far too long. That’s when we turned to Brieflly. In less than 10 minutes, their brief creation tool helped us generate a clear, detailed project scope, complete with tasks and budget estimates. Brieflly then matched us with a pre-vetted creative agency that fit our exact needs. Thanks to Brieflly, we launched the project 50% faster than expected and, thanks to the platform’s transparent pricing, we even came in 20% under budget. Brieflly has completely transformed the way we handle projects."',
                    image: 'https://codingyaar.com/wp-content/uploads/square-headshot-2.png',
                    name: 'June Doe',
                    company: 'CEO, Example Company',
                },
                {
                    title: 'New Website design Time by 90% and Came in 10% Under Budget',
                    description:
                        '"We were struggling to find a reliable agency for our website redesign, and the manual vetting process was taking far too long. That’s when we turned to Brieflly. In less than 10 minutes, their brief creation tool helped us generate a clear, detailed project scope, complete with tasks and budget estimates. Brieflly then matched us with a pre-vetted creative agency that fit our exact needs. Thanks to Brieflly, we launched the project 50% faster than expected and, thanks to the platform’s transparent pricing, we even came in 20% under budget. Brieflly has completely transformed the way we handle projects"',
                    image: 'https://codingyaar.com/wp-content/uploads/bootstrap-profile-card-image.jpg',
                    name: 'John Doe',
                    company: 'CEO, Example Company',
                },
                {
                    title: '30% Increase in Lead Generation with the Right Marketing Team',
                    description:
                        '"We were struggling to find a reliable agency for our website redesign, and the manual vetting process was taking far too long. That’s when we turned to Brieflly. In less than 10 minutes, their brief creation tool helped us generate a clear, detailed project scope, complete with tasks and budget estimates. Brieflly then matched us with a pre-vetted creative agency that fit our exact needs. Thanks to Brieflly, we launched the project 50% faster than expected and, thanks to the platform’s transparent pricing, we even came in 20% under budget. Brieflly has completely transformed the way we handle projects."',
                    image: 'https://codingyaar.com/wp-content/uploads/square-headshot-2.png',
                    name: 'June Doe',
                    company: 'CEO, Example Company',
                },
                {
                    title: 'New Website design Time by 90% and Came in 10% Under Budget',
                    description:
                        '"We were struggling to find a reliable agency for our website redesign, and the manual vetting process was taking far too long. That’s when we turned to Brieflly. In less than 10 minutes, their brief creation tool helped us generate a clear, detailed project scope, complete with tasks and budget estimates. Brieflly then matched us with a pre-vetted creative agency that fit our exact needs. Thanks to Brieflly, we launched the project 50% faster than expected and, thanks to the platform’s transparent pricing, we even came in 20% under budget. Brieflly has completely transformed the way we handle projects"',
                    image: 'https://codingyaar.com/wp-content/uploads/bootstrap-profile-card-image.jpg',
                    name: 'John Doe',
                    company: 'CEO, Example Company',
                },
            ],
        }
    },
}
</script>
