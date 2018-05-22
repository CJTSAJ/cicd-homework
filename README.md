# CI/CD环境搭建与使用

#### 组员：陈江涛、方娄昊、刘泽宇、李琥、贾兴国
## CI
### CI的好处
- 减少项目的风险,尽早发现并修复bug,尽早估量软件质量
- 产生可部署的软件,让项目组在任一点上及时提交可以安装的软件包
- 自动化的持续集成可以减少重复性的劳动，节约时间，提高效率

### 使用Travis CI实现CI
*Travis CI 是在软件开发领域中的一个在线的，分布式的持续集成服务，用来构建及测试在GitHub托管的代码。*
#### 流程
1. 登录github并创建一个项目，本小组使用vue.js框架的前端项目
![](https://github.com/CJTSAJ/cicd-homework/blob/master/PPT_pic/1.png)

2. 前往Travis CI官网，登录github账号，开启对项目的集成
![](https://github.com/CJTSAJ/cicd-homework/blob/master/PPT_pic/2.png)

3. 在项目中创建相应的.travis.yml配置文件。针对该项目，语言为node_js,测试代码前运行<code>npm install</code>指令，测试时运行<code>npm test</code>指令，测试的结果会发送到邮箱

![](https://github.com/CJTSAJ/cicd-homework/blob/master/PPT_pic/3.png)

4. 上传.travis.ci文件后，项目就开始自动构建并运行测试
![](https://github.com/CJTSAJ/cicd-homework/blob/master/PPT_pic/4.png)


## CD
### CD的好处
- 缩短 编码->测试->上线->交付 的迭代周期，快速交付高质量的产品

### 使用Heroku实现CD
*Heroku平台是一个支持多种语言的服务，能通过git push把程序推送到heroku的git服务器上，在服务器上进行安装、配置和部署程序。*
#### 流程
1. 在Heroku官网上注册并下载heroku-cli
2. 登录heroku   <code>heroku login</code>
创建仓库
<code>heroku create</code>
3. 打开命令行，在本地Vue项目文件夹中运行<code>npm run build</code>命令，生成静态文件并放在dist文件夹中
4.  暂存修改并提交
<code> git add </code>
	 <code> git commit</code>
5. 将本地仓库修改推送并部署到heroku
<code>git push heroku master</code>
6. 运行部署的网站
<code> heroku open</code>
效果如图
![](https://github.com/CJTSAJ/cicd-homework/blob/master/PPT_pic/8.png)

### 使用Github Pages实现CD
[Repo地址](https://github.com/CJTSAJ/travis-pages-homework)






























