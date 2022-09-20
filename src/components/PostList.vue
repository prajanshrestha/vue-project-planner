<template>
  <div class="post-list">
    <div v-for="post in posts" :key="post.id">
        <single-post :post="post"></single-post>
    </div>
  </div>
</template>

<script>
import { onMounted, onUnmounted, onUpdated } from '@vue/runtime-core';
import SinglePost from "./SinglePost.vue";

export default {
    components: {
        SinglePost
    },
    props: {
        posts: {

        }
    },
    setup(props) {
        console.log(props.posts);   
        onMounted(() => console.log("component mounted"));
        onUnmounted(() => console.log("component unmounted"));
        onUpdated(() => console.log("component updated"));
    }
}
</script>

<style>

</style>