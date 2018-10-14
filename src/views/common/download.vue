<template>
    <div id="download">
        <el-table :data="tableData" style="width: 100%;">
            <el-table-column label="名称" width="150" prop="name"></el-table-column>
            <el-table-column label="上传时间" width="150" prop="date"></el-table-column>
            <el-table-column label="下载" width="150">
                <template slot-scope="scope">
                    <el-button type="text" size="small">下载</el-button>
                </template>
            </el-table-column>
        </el-table>
        
    </div>
    
</template>


<script>
export default {
    name: 'Download',
    data() {
        return {
            tableData: [{
                name: 'js基础',
                date: '2018-01-01'
            },
            {
                name: 'react-js',
                date: '2018-01-01'
            },
            {
                name: 'vue-js',
                date: '2018-01-01'
            },
            {
                name: 'node-js',
                date: '2018-01-01'
            }]
        };
    },
    methods: {}
};
</script>
<style scoped>
    #download{
        margin: 0 auto;

    }
    el-table{
        margin: 0 auto;
        width:100%;
        border:5px solid #ddd;
        background-color: pink;
    }
</style>

