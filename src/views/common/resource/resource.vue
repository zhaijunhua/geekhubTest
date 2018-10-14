<template>
    <div>
            <h1>这里是资源页面</h1>
            <Restwo/>
            <Resone/>
    </div>
</template>
<script>
import Resone from './resource1.vue';
import Restwo from './resource2.vue';
export default {
    name: 'Resource',
    components: {
        Resone,
        Restwo
    },
    data() {
        return {
            sourceName: [
                {text: '博客文档'},
                {text: '代码下载'},
                {text: '百度云资源'}
            ]
        };
    }
};
</script>
