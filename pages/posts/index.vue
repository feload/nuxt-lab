<template>
    <div class="posts-page">
        <template v-for="post in posts">
            <PostPreview
                :title="post.title"
                :thumbnail="post.thumbnail"
                :previewText="post.previewText"
                :id="post.id"
                :key="post.id" />
        </template>
    </div>
</template>

<script>
import PostPreview from '~/components/PostPreview'

export default {
    // This works only on pages, not in individual components.
    asyncData() {
        return new Promise((res, rej) => {
            setTimeout(() => {
                res({
                    posts: [
                    {
                        id: Math.random().toString(),
                        title: 'Title of post',
                        thumbnail: 'null',
                        previewText: 'Preview text'
                    },
                    {
                        id: Math.random().toString(),
                        title: 'Title of post',
                        thumbnail: 'null',
                        previewText: 'Preview text'
                    }
                    ]
                })
            }, 2000)
        });
    },

    components: {
        PostPreview
    }
}
</script>


<style scoped>
.posts-page {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>

