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
                    question: "How does Brieflly match my agency with clients?",
                    answer: "Brieflly’s matching technology uses data-powered analytics to assess each brief’s specific requirements and match them to agencies with the right experience, expertise, and proven track record. You only see projects that genuinely fit, so you spend less time searching and more time on high-impact work."
                },
                {
                    question: "What is the vetting process for agencies?",
                    answer: "Every agency goes through a rigorous vetting process. Our team evaluates your client history, expertise, and past project success to ensure our users are matched with trusted, high-quality agencies. Only agencies that pass Brieflly’s rigorous vetting make it in, creating a network built on trust and proven expertise."
                },
                {
                    question: "How does payment work?",
                    answer: "Brieflly offers milestone-based payments, so you get paid as each stage is completed. This system reduces invoicing issues, aligns payments with project progress, and boosts cash flow reliability for your agency."
                },
                {
                    question: "How much does it cost to join?",
                    answer: "Agencies join Brieflly for free. Project costs are handled through a flexible, credit-based system managed by clients, so you only focus on delivering great work without extra fees."
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
