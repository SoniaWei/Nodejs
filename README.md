# Nodejs
Nodejs开发实战

BFF层 Backend for Fontend 
能让前端有能力处理数据，在搭建过程中的RPC调用都需要后端和运维的紧密配合

## 什么事nodejs  
官网：  
>node.js是一个基于**chorme V8引擎**的javascript运行环境  
>node.js是使用了一个**事件驱动**、**非阻塞式I/O**的模型，使其轻量又高效  

chorme浏览器用的同样是JavaScript引擎和模型  
**其实，在Node.JS里面写js和在chorme里写js，几乎没有不一样**  
node.js没有浏览器api 
加了许多node api  

## node.js可以用来做什么  
+ seo优化  
+ 加速网页首屏渲染  

### 构建工作流  
+ 构建工具不会永远不出问题  
+ 构建工具不会永远满足需求

### 开发工具 - VS Code
大型应用需要给使用者自定义模块的能力  
使用Node.js做复杂本地应用  
+ 可以利用JS的灵活性提供外部扩展  
+ JS庞大的开发者基数让他们的灵活性得到利用  
+ 在已有网站的情况下需要新发开客户端应用  
+ 用Node.js客户端技术（electron）实现，最大限度复用现有工程  

## 实战  
+ 列表页  
  + 打通前后台  
  + 服务端渲染  
+ 详情页  
  + 网页路由  
  + 异步加载  
+ 播放页  
  + api服务器  
  
## 技术预研  
+ BFF层  
  + 对用户侧提供HTTP服务  
  + 使用后端RPC 服务  

## 实战 -- 石头剪刀布游戏  
```
console.log(_filename_)
console.log(_dirname_)
console.log(process)
```

```
var playerAction = process.argv[process.argv.length -1];
console.log(playerAction)
var random = Math.random() * 3;
if(random < 1) {
  var computerAction = 'rock'
} else if (random > 2) {
  var computerAction = 'scissor'
} else  {
  var computerAction = 'paper'
}
if (computerAction == playerAction) {
  console.log("平局")
} else if (
  (computerAction == "rock" && playerAction == "paper") || 
  (computerAction == "scissor" && playerAction == "rock") || 
  (computerAction == "paper" && playerAction == "scissor") 
) {
  console.log("你赢了")
} else {
  console.log("你输了")
}
```
