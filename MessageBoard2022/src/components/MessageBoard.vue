<template>
  <div id="message-board">
    <el-container style="height:100%; border: 1px solid #eee">
      <el-header style="text-align: right; font-size: 10px">
        <el-button style="display: inline-block;margin-right: 15px;" v-on:click="postDialog.dialogVisible=true">
          <i class="el-icon-edit">发表</i>
        </el-button>
        <!--请修改这两行注释中间的代码完成"刷新"功能-->
        <el-button style="display: inline-block;margin-right: 15px;">
        <!--请修改这两行注释中间的代码完成"刷新"功能-->
          <i class="el-icon-refresh" style="object-fit: fill">刷新</i>
        </el-button>
        <el-dropdown trigger="click">
          <el-button><i class="el-icon-user" style="object-fit: contain">
            <span v-if="state.username_valid">{{state.username}}</span>
            <span v-else>匿名</span></i>
          </el-button>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item v-if="state.username_valid">
              <a v-on:click="clearUserName()">注销</a>
            </el-dropdown-item>
            <el-dropdown-item v-if="state.username_valid">
              <a v-on:click="loginDialog.dialogVisible=true">修改</a>
            </el-dropdown-item>
            <el-dropdown-item v-if="!state.username_valid">
              <a v-on:click="loginDialog.dialogVisible=true">设置</a>
            </el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-header>

      <el-main>
        <!--请补全这两行注释中间的messagelist-->
		
        <MessageList/>
		
        <!--请补全这两行注释中间的messagelist-->
      </el-main>

      <el-footer>@CST2021SE</el-footer>
    </el-container>
    <!--请补全这两行注释中间的PostDialog-->
    <PostDialog/>
    <!--请补全这两行注释中间的PostDialog-->
    <!--请补全这两行注释中间的LoginDialog-->
    <LoginDialog/>
    <!--请补全这两行注释中间的LoginDialog-->
    <el-dialog
            style="text-align: center"
            :title="alertDialog.text"
            :visible.sync="alertDialog.dialogVisible"
            width="40%">
    </el-dialog>
  </div>
</template>

<script>
import MessageList from "@/components/MessageList"
import PostDialog from "@/components/PostDialog"
import LoginDialog from "./LoginDialog";
export default {
	name: "MessageBoard",
	components: {
    LoginDialog,
		MessageList,
		PostDialog
	},
	// 请在下方设计自己的数据结构及函数来完成最终的留言板功能
	data(){
		return {
			postDialog:{
				dialogVisible:false
			},
      loginDialog:{
        dialogVisible:false,
        dialogError:"",
        form:{
          username:""
        }
      },
			alertDialog:{
				"text":"",
				dialogVisible:false
			},
			state:{
				username:  "",
				username_valid:false
			},
			messageList: []
		}
	},
	methods:{
    clearUserName:()=>{
      //补全代码时可以使用utils/tool。js的代码
    }
	},
  watch: { // 用于实时检测username是否合法
    "state.username": {
      handler(newName) {
        this.state.username_valid = /^[A-Za-z\u4e00-\u9fa5][-A-Za-z0-9\u4e00-\u9fa5_]*$/.test(newName)
      }
    }
  }
}
</script>

<style scoped>
    #message-board{
        height: calc(100vh - 16px);
    }
    .message-tab{
        display: block;
        padding: 10px;
        text-align: left;
    }
    .el-header {
        background-color: #B3C0D1;
        color: #333;
        line-height: 60px;
    }
    .el-footer {
        background-color: #7197c9;
        color: #333;
        line-height: 60px;
    }
    .el-aside {
        color: #333;
    }
</style>
