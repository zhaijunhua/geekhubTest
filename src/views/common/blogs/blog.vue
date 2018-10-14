<template>
    <div id="blog">
        <div class="blog-content">
            <el-table :data="tableData.slice((currentPage-1)*pagesize,currentPage*pagesize)">
                <el-table-column label="名称" width="150" prop="blogName"></el-table-column>
                <el-table-column label="作者" width="100" prop="author"></el-table-column>
                <el-table-column label="上传时间" width="150" prop="uploadTime"></el-table-column>
            </el-table>
            <el-pagination class="fy"
                     layout="prev, pager, next"
                     @current-change="current_change"
                     :total="total"
                     background
                    >
                  </el-pagination>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Blog',
    data() {
        return {
            total: 50,
            pagesize: 3,
            currentPage: 1,
            istag: true,
            tableData: [
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tony',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tony',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tony',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'jhon',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'TIhon',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                },
                {
                    blogName: '浅谈nodejs',
                    author: 'Tom',
                    uploadTime: '2018-1-1'
                }]
        };
    },
    methods: {
        created: function(tableData) {
            this.total = tableData.length;
        },
        current_change: function(currentPage) {
            this.currentPage = currentPage;
        }
    }
};
</script>
<style>
.time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }
.clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }
  el-col{
      margin: 0 auto;
  }
</style>

