<template>
    <div id="restwo">
       <el-button type="info" @click="chat">显示</el-button>
    </div>
    
</template>


<script>
import Chat from '../../../assets/chat.js';
export default {
    name: 'Restwo',
    data() {
        return {
            message: ''
        };
    },
    methods: {
        chat() {
            Chat.$emit('msg', '这里是resource2');
        }
    },
    props: ['todo']
};
</script>
