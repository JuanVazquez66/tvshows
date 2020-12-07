<!--    Popular Tv Shows
        Name: Juan Vazquez
        Teacher: Kirsten Markley
        Class: cis-131-w01
        Date: 12/6/20
-->

<!--new component for Header-->
<template>
    <div class="header">
        <h1>{{headerTitle}}</h1>
    </div>
</template>

<script>
export default {
    name: "Header",
    props: ['headerTitle']
}
</script>

<style scoped>
    .header {
        background: #333;
        color: white;
        text-align: center;
        padding: 20px;
        margin: 0px;
        margin-top: 0px;
    }
</style>