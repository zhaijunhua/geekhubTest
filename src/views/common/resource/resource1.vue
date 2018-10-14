<template>
    <div id="one">
        <div id="receive">
            <p>{{message}}</p>
        </div>
    </div>
</template>
<script>
import Chat from '../../../assets/chat.js';

export default {
    name: 'Resone',
    data() {
        return {
            message: ''
        };
    },
    mounted() {
        let brother = this;
        Chat.$on('msg', (e) => {
            brother.message = e;
        });
    }
};
</script>
