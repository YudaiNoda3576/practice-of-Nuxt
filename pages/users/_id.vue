<template>
    <section>
        <h1>{{ message }}</h1>
        <p>id: {{ this.$route.params.id }}</p>
    </section>
</template>

<script>
export default {
    data: function() {
        return {
            message: "/users/_id.vueを表示中",
        };
    },
    validate({ params }) {
        const regex = new RegExp('[0-9０-９]+');
        return regex.test(params.id)
    }
};
</script>