<template>
    <div :style="wrapperStyle">
        <img :src="src" :style="imgStyle"/>
        <span :style="textStyle"><slot></slot></span>
    </div>
</template>

<script>
export default{
    props:{
        wrapperStyle: Object,
        src: String,
        imgStyle: Object,
        textStyle: Object,
    }
}
</script>