<template>
    <section>
        <div class="container">
            <div class="row text-center">
                <div class="col">
                    <h2 class="display-5">Your Questions, Answered</h2>
                </div>
            </div>
            <div class="row">
                <div class="col mt-5">
                    <div class="accordion accordion-flush" id="faqs">
                        <div class="accordion-item py-4" v-for="(faq, index) in faqs" :key="index">
                            <h3 class="accordion-header">
                                <button class="accordion-button" :class="{ collapsed: !isActive(index) }" type="button"
                                    @click="toggle(index)">
                                    {{ faq.question }}
                                </button>
                            </h3>
                            <div :id="'collapse' + index" class="accordion-collapse"
                                :class="{ collapse: !isActive(index), show: isActive(index) }">
                                <div class="accordion-body text-secondary">
                                    {{ faq.answer }}
                                </div>
                            </div>
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
            activeIndex: null,
            faqs: [
                {
                    question: "How does Brieflly match me with the right service provider?",
                    answer: "Brieflly uses a sophisticated, data-driven algorithm that instantly matches your project brief with vetted and verified service providers who meet your specific needs. No more searching, Brieflly does the heavy lifting for you."
                },
                {
                    question: "What are Brieflly’s pricing plans?",
                    answer: "We offer a variety of plans to suit different needs and budgets. Here’s an overview: Free Plan: $0/month, includes 10 free credits to try out the platform. Basic Plan: $8.99/month, ideal for smaller projects. Explorer Plan: $14.99/month, offering better credit discounts for medium-level usage. Pro Plan: $24.99/month, the best value for high-volume users. Each plan allows you to purchase credit packages at discounted rates, with larger packages offering the best value."
                },
                {
                    question: "How do I pay with Brieflly’s credit system?",
                    answer: "It’s simple: you purchase credits based on the package that fits your needs. Use these credits to create briefs, match with experts, and manage your projects. Running a bigger project? Simply add more credits - pay only for what you need, with no hidden costs."
                },
                {
                    question: "How do I know the providers on Brieflly are reliable?",
                    answer: "Every expert on our platform is vetted and verified. We dive deep into their work history, reviews, and expertise so you don’t have to. When Brieflly says 'expert,' we mean it, you’re in safe hands every time."
                }
            ]
        };
    },
    methods: {
        toggle(index) {
            this.activeIndex = this.activeIndex === index ? null : index;
        },
        isActive(index) {
            return this.activeIndex === index;
        }
    }
};
</script>

<style scoped>
.accordion-button {
    cursor: pointer;
    border: none;
    background-color: transparent;
    text-align: left;
    width: 100%;
    padding: 1em;
}

.accordion-button.collapsed {
    transform: rotate(0deg);
}

.accordion-collapse {
    transition: max-height 0.3s ease;
    overflow: hidden;
}

.accordion-collapse.collapse {
    max-height: 0;
}

.accordion-collapse.show {
    max-height: 1000px;
    /* Arbitrary large value */
}
</style>
