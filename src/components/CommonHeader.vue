<template>
<el-header>
    <div class="l-content">
        <el-button size="small" plain @click="handleCollapse">
            <el-icon :size = "20">
                <Menu />
            </el-icon>
        </el-button>
        <h3> 首页 </h3>
    </div>
    <div class="r-content">
    <el-dropdown>
    <span class="el-dropdown-link">
      <img class ="user" :src="getImgSrc()" alt="" />
    </span>
    <template #dropdown>
      <el-dropdown-menu>
        <el-dropdown-item>个人中心</el-dropdown-item>
        <el-dropdown-item> 退 出 </el-dropdown-item>
        
      </el-dropdown-menu>
    </template>
  </el-dropdown>
    </div>
</el-header>
  </template>
  <script>
    export default {
        setup(){
           const getImgSrc = () =>{
            return new URL('../assets/images/123.jpeg',import.meta.url).href;
           }
            return {
                //imgSrc,
                getImgSrc,
            };

            },
    };
  </script>

  <style lang="less" scoped>

    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        background-color: rgb(41, 53, 53);

    }
    .r-content{
        .user{
            width: 40px;
            height: 40px;
            border-radius: 50%;
        }
    }
    .l-content{
        display: flex;
        align-items: center;
        h3{
            color: antiquewhite;
        }
        .el-button{
            margin-right: 20px;
        }
    }
  </style>