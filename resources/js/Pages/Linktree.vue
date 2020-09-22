<template>
    <app-layout>
        <LinktreeList :username="username">We are test</LinktreeList>
    </app-layout>
</template>

<script>
    import AppLayout from './../Layouts/PublicAppLayout'
    import LinktreeList from './../Linktree/List'
    export default {
        props: {
            'username': '',
        },
        components: {
            AppLayout,
            LinktreeList,
        },
    }
</script>
