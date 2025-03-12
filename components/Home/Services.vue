<template>
    <section>
        <div class="container py-5">
            <div class="row text-center">
                <div class="col" data-aos="fade-in">
                    <h2 class="display-5">Match With The Right Experts, Right Now</h2>
                </div>
            </div>
            <div class="row mt-5">
                <div v-for="(service, index) in services" :key="index" class="col-md-6 col-lg-4 my-4">
                    <div class="card bg-light border-light-subtle shadow-sm rounded-4 py-3 h-100" data-aos="fade-in">
                        <div class="card-body">
                            <h3 class="lead fw-bold mb-3">
                                <img :src="`/img/home/services/${service.icon}.png`" width="60" height="60" :alt="service.name">
                                <span class="ms-2">
                                    {{ service.name }}
                                </span>
                            </h3>
                            <ul>
                                <li v-for="(subService, subIndex) in service.subServices" :key="subIndex">
                                    {{ subService }}
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const services = [
    {
        name: 'Development',
        icon: 'development',
        subServices: [
            'Mobile App Development',
            'Software Development',
            'Web Development',
            'AR/VR',
            'Artificial Intelligence',
            'Blockchain'
        ]
    },
    {
        name: 'Design & Production',
        icon: 'design-and-production',
        subServices: [
            'Web Design',
            'User Experience Design',
            'Logo Design',
            'Graphic Design',
            'Design',
            'Digital Design'
        ]
    },
    {
        name: 'Marketing',
        icon: 'marketing',
        subServices: [
            'Digital Marketing',
            'SEO',
            'Social Media Marketing',
            'Mobile Marketing',
            'Content Marketing',
            'Search Marketing'
        ]
    },
    {
        name: 'Advertising',
        icon: 'advertising',
        subServices: [
            'Advertising',
            'Branding',
            'Creative',
            'Video Production',
            'Public Relations',
            'Media Planning & Buying'
        ]
    },
    {
        name: 'Business Services',
        icon: 'business-services',
        subServices: [
            'Call Centers',
            'BPO',
            'Accounting',
            'Commercial Real Estate',
            'HR Services',
            'Consulting'
        ]
    },
    {
        name: 'IT Services',
        icon: 'it-services',
        subServices: [
            'IT Services',
            'Cybersecurity',
            'Data Analytics',
            'Managed IT Services',
            'Cloud Consulting',
            'Staff Augmentation'
        ]
    }
]
</script>

