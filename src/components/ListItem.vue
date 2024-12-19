<template>
    <li>
        <img :src="require(`@/assets/images/${icon}`)" :alt="icon">
        <span>{{ text }}</span>
    </li>
</template>

<script>
export default {
    props: {
        text: {
            type: String,
            required: false
        },
        icon: {
            default: 'user.png'
        }
    }
}
</script>