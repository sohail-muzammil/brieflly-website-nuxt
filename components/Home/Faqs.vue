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
                    answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste deleniti nam pariatur iusto repellat vitae sint fugiat. Soluta, eligendi voluptates. Est at dolore nemo quam repellat ea alias possimus eaque?"
                },
                {
                    question: "What are Brieflly’s pricing plans?",
                    answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste deleniti nam pariatur iusto repellat vitae sint fugiat. Soluta, eligendi voluptates. Est at dolore nemo quam repellat ea alias possimus eaque?"
                },
                {
                    question: "How do I pay with Brieflly’s credit system?",
                    answer: "It’s simple: you purchase credits based on the package that fits your needs. Use these credits to create briefs, match with experts, and manage your projects. Running a bigger project? Simply add more credits - pay only for what you need, with no hidden costs."
                },
                {
                    question: "How do I know the providers on Brieflly are reliable?",
                    answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste deleniti nam pariatur iusto repellat vitae sint fugiat. Soluta, eligendi voluptates. Est at dolore nemo quam repellat ea alias possimus eaque?"
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
