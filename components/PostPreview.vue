<template>
    <div class="post-preview">
        <h4>{{ title }}</h4>
        <p>{{ previewText }}</p>
    </div>
</template>
<script>
export default {
    name: 'PostPreview',
    props: {
        id: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required: true
        },
        previewText: {
            type: String,
            required: true
        },
        thumbnail: {
            type: String,
            required: true
        }
    }
}
</script>
