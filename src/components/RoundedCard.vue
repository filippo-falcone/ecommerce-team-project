<script>
export default {
    props: {
        cardInfo: Object
    }
}
</script>
<template>
    <div class="hstack">
        <div class="vstack">
            <img :src="cardInfo.image" alt="">
        </div>
    </div>

</template>

<style lang="scss"></style>