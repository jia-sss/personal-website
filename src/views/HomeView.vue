<script setup lang="ts">
import { onMounted } from 'vue'

onMounted(() => {
    // @ts-ignore
    twikoo.init({
        envId: 'https://pinglun.jiaoo.cc',
        el: '#comment'
    })
})
</script>

<template>
    <main>
        <div class="rainbow">
            <span>我不知道这个网站要干什么。。。</span>
        </div>
        <div class="comment">
            <p style="font-size: 25px; font-family: b">提个建议。</p>
            <div id="comment"></div>
            <span id="twikoo_visitors">0</span>
        </div>
    </main>
</template>
<style>
@font-face {
    font-family: 'a';
    src: url('../assets/a.woff2');
}
@font-face {
    font-family: 'b';
    src: url('../assets/b.woff2');
}
@font-face {
    font-family: 'c';
    src: url('../assets/c.woff2');
}
@font-face {
    font-family: 'd';
    src: url('../assets/d.woff2');
}
.rainbow {
    background: linear-gradient(to right, red, yellow, lime, aqua, blue, fuchsia) 0 / 50%;
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: hue 6s infinite;

    font-size: 5rem;
    text-align: center;
    min-height: 260px;
    font-family: d;
    white-space: wrap;
    display: flex;
    align-items: center;
    justify-content: center;
}
@keyframes hue {
    from {
        filter: hue-rotate(0deg);
    }
    to {
        filter: hue-rotate(360deg);
    }
}
.comment {
    max-width: 760px;
    margin: auto;
}
</style>
