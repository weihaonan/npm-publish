### 操作
#### 1、发布npm包之前得有自己的npm账号，可以在npm注册，也可以在命令提示符创建用户，在这里我们直接用命令提示符创建（如果已经有npm账号可以跳过）,直接在目录下输入npm adduser命令，根据提示依次输入用户名、密码、邮箱（如果已经有了npm账户，输入npm login命令）
![](https://github.com/weihaonan/npm-publish/blob/master/img/1.bmp)

#### 2、创建npm用户后，需要去注册邮箱进行激活，完后才可以发布
#### 3、激活之后，就可以直接发布，输入npm publish命令
![](https://github.com/weihaonan/npm-publish/blob/master/img/3.bmp)

#### 4、发布成功后，登入npm会发现多了一个package,然后就可以使用npm i whnbag-npm-test引入这个包
![](https://github.com/weihaonan/npm-publish/blob/master/img/5.bmp)
#### 补充
##### 1、如果npm login时候报 Unable to authenticate, need:Basic错误，可以在输入username时加一个~符号试试
##### 2、如果想更新这个npm包，只需在package.json文件中修改version，再重新npm pu  

##### 3、npm包的查找规则：（1）在项目根目录中查找有没有node_modules 的文件夹（2）在node_modules 中，根据包名，找对应的vue文件夹（3）在vue文件夹中，找一个叫做package.json的包配置文件（4）在package.json文件中，查找一个main属性【main属性指定了这个包在被加载的时候  的入口文件】 
##### 4、修改npm包的查找路径：（1）import Vue from '../node_modules/*/*'（2）在包的package.json文件中main属性指定的入口文件修改为【"main": "*/*/",】（3）在项目的webpack.config.js中添加resolve属性,例如:resolve:{alias: {"vue$" : "vue/dist/vue.js"}}

