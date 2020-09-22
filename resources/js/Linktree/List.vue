<template>
    <div>
        <draggable tag="ul" ghost-class="moving-card" class="w-full" :list="users" :animation="200">
            <li v-for="user in users"
                :key="user.id"
                class="p-4 mb-3 flex justify-between items-center bg-white shadow rounded-lg cursor-move">
                {{user.name}}
            </li>
        </draggable>
    </div>
</template>

<script>
    import Draggable from 'vuedraggable'
    export default {
        components: {
            Draggable
        },
        props: {
            username: ''
        },
        data() {
            return {
                users: [
                {
                    id: 1,
                    name: "Latest Video",
                    url: "https://www.youtube.com"
                },
                {
                    id: 2,
                    name: "Twitter Post",
                    url: "https://www.twitter.com"
                },
                {
                    id: 3,
                    name: "Some other",
                    url: "https://www.someother.com"
                },
                {
                    id: 4,
                    name: "Blabla Blablab",
                    url: "https://www.bla.com"
                },
            ]
            }
        }
    }
</script>

<style>
    .moving-card {
        @apply opacity-50 bg-gray-100 border border-blue-500;
    }
</style>