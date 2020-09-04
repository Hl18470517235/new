<template>
    <div id="mainviews">
    <LayouHeader></LayouHeader>
    <LayouMain></LayouMain>
    <LayouNav></LayouNav>
    </div>
</template>

<script>
import LayouHeader from '../components/LayouHeader'
import LayouMain from '../components/LayouMain'
import LayouNav from '../components/LayouNav'
export default {
    name:"mainviews",
    components:{LayouHeader,LayouMain,LayouNav}
}
</script>

<style>

</style>