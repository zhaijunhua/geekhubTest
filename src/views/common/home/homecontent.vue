<template>
    <div id="homecontent">
        <el-button type="info" v-on:click="sendMessage">这是来自homeconent的问候</el-button>
        <ul>
            <li v-for="sorts in sort" v-on:click="sorts.show=!sorts.show">
                <h2>{{sorts.name}}</h2>
                <h3 v-show="sorts.show">{{sorts.position}}</h3>
            </li>
        </ul>
    </div>
    
</template>

<script>
export default {
    name: 'Homecontent',
    props: ['sort'],
    data() {
        return {};
    },
    methods: {
        deleteUser: function() {
            this.sort.pop();
        },
        sendMessage: function() {
            this.$emit('getMessage', 'welcome to this hub');
        }
    }
};
</script>
<style scoped>
#homecontent{
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
