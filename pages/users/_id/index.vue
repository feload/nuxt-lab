<template>
    <div class="users users__user">
        A single user {{ $route.params.id }}
    </div>
</template>
<script>
export default {
    validate(data) {
        return /^\d+$/.test(data.params.id)
    }
}
</script>
