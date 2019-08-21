<!--
 * @Description: In User Settings Edit
 * @Author: your name
 * @Date: 2019-08-05 14:54:16
 * @LastEditTime: 2019-08-19 11:05:32
 * @LastEditors: Please set LastEditors
 -->
 ## Startalk Web
### 简介
- Startalk Web是网页版聊天工具
### 安装
  #### 环境要求
  - node@ >= 8.6.0
  - pm2 @>= 2.0.0

  #### 项目启动开发
  - git clone https://github.com/qunarcorp/startalk_web.git 克隆代码到本地
  - npm install 安装项目依赖
  - 修改 .env 文件为 NODE_ENV=development
  - profiles/development/startalk.env 配置后台地址，
    如： BASEURL=http://127.0.0.1:8080
  - 执行 npm run build , 新开 tab 页执行 npm run dev 启动项目

  #### 项目打包上线
  - 修改 .env 文件为 NODE_ENV=production
  - profiles/development/startalk.env 配置线上环境后台地址，
    如： BASEURL=http://127.0.0.1:8080
  - npm run build
  - npm run client

### 初始化账号密码： admin/testpassword


### 书写规范
  - 驼峰命名
  - 中英文之间空格
  - 不写分号

### 注意事项
  #### 1.模块化引用,减少包的体积
  - 比如lodash
  - import omit from 'lodash/omit' //best
  - import { omit } from 'lodash'  //bad

  #### 2.获取直属领导，员工编号和查询用户电话功能
  - 两个功能的逻辑已写好
  - 接口需使用者自己实现,位置位于entry.js