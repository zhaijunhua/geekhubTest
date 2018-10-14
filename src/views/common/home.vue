<template>
    <div class="home">
        <!-- 绑定属性 -->
        <home-content v-bind:sort="sort" v-on:getMessage="showMessage"></home-content>
    </div>
    
</template>

<script>
import homecontent from './home/homecontent.vue';
export default {
    name: 'home',
    data() {
        return {
            sort: [
                {
                    name: 'javascript',
                    position: '前端开发',
                    show: false
                },
                {
                    name: 'vue',
                    position: '前端开发',
                    show: false
                },
                {
                    name: 'react',
                    position: '前端开发',
                    show: false
                },
                {
                    name: 'node',
                    position: '前端开发',
                    show: false
                },
                {
                    name: 'Spring',
                    position: 'java开发',
                    show: false
                },
                {
                    name: 'java',
                    position: 'java开发',
                    show: false
                }],
            welcomeWord: 'welcome to this hub!'
        };
    },
    components: {
        'home-content': homecontent
    },
    methods: {
        showMessage: function(data) {
            alert(data);
        }
    }
};
</script>
<style scoped>
.user{
    width:100%;
    max-width: 1200px;
    padding: 0 20px;
    box-sizing: border-box;
    margin: 40px auto;
}
ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding:0;

}
li{
    width: 100%;
    flex-grow: inherit;
    border: 1px solid #222;
    flex-basis: 200px;
    text-align: center;
    padding: 30px;
    margin: 10px;
}



</style>
