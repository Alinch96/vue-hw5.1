<template>
    <li class="raspberry-item">
        <div class="img-wrapper">
            <img :src="raspberry.imgSrc" :alt="raspberry.description" />
        </div>
        <div class="company-wrapper">
            <img :src="raspberry.logo" :alt="`${raspberry.companyTitle}logo`" />
            <p class="company-title">{{ raspberry.companyTitle }}</p>
            <p v-if="raspberry.isPresent" class="green">В наявності</p>
        </div>

        <h3 class="raspberry-description">{{ raspberry.description }}</h3>

    </li>
</template>

<script>
export default {
    name: "RaspberryItem",
    props: {
        raspberry: {
            type: Object,
            required: true,
        },
    },
};
</script>

<style lang="scss" scoped>
.raspberry-item {
    display: flex;
    flex-direction: column;
    gap: 12px;
    padding: 20px;
    align-items: flex-start ;
}

.img-wrapper {
    width: 100%;
    height: 200px;
    border-radius: 8px;
    overflow: hidden;
    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
.company-wrapper {
    display: flex;
    gap: 8px;
    align-items: center;

    img {
        width: 15px;
        height: 15px;
    }
    .company-title {
        font-size: 18px;
        font-weight: 700;
    }
    .green {
        color: green;
    }
}
.raspberry-description {
    font-size: 20px;
}
</style>