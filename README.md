# TGeditor
这是一个简单的富文本编辑器  

纯JavaScript，不需担心和其他插件冲突。

## 用法
### 引用：
```
<link rel="stylesheet" href="fontAwesome/css/font-awesome.min.css">  
<link rel="stylesheet" href="richEditor.css">  
<script src="richEditor.min.js"></script>
```

### 布局
在页面放一个编辑器div（目前只支持这种方式）：  
```
<div id="editor">       
  <p>这是一个富文本编辑器，简单高效！</p>       
  <p>你可以通过getHTML()获取编辑器中的所有内容，也可以通过getText()获取纯文本内容</p>    
</div>
``` 

### 调用
```
var editor = new RichEditor("#editor", {
		width:900,
		height:400,
		toolBg:"#eee",
		buttons: {
				heading:{
					title:"标题",
					icon:"\uf1dc"
				},
				code: {
					title: "引用",
					icon: "\uf10d"
				},
				bold: {
					title: "加粗",
					icon: "\uf032"
				},
				italic: {
					title: "斜体",
					icon: "\uf033"
				},
				underline: {
					title: "下划线",
					icon: "\uf0cd"
				},
				strikethrough: {
					title: "删除线",
					icon: "\uf0cc"
				},
				foreColor: {
					title: "字体颜色",
					icon: "\uf1fc"
				},
				backColor: {
					title: "背景色",
					icon: "\uf043"
				},
				justifyLeft: {
					title: "居左",
					icon: "\uf036"
				},
				justifyCenter: {
					title: "居中",
					icon: "\uf037"
				},
				justifyRight: {
					title: "居右",
					icon: "\uf038"
				},
				justifyFull: {
					title: "两端对齐",
					icon: "\uf039"
				},
				insertOrderedList: {
					title: "有序列表",
					icon: "\uf0cb"
				},
				insertUnorderedList: {
					title: "无序列表",
					icon: "\uf0ca"
				},
				indent:{
					title:"indent",
					icon:"\uf03c"
				},
				outdent:{
					title:"outdent",
					icon:"\uf03b"
				},
				createLink: {
					title: "链接",
					icon: "\uf0c1"
				},
				insertImage: {
					title: "插入图片",
					icon: "\uf03e"
				},
				emotion: {
					title: "表情",
					icon: "\uf118"
				},
				fullscreen: {
					title: "全屏",
					icon: "\uf066"
				},
				save: {
					title: "保存",
					icon: "\uf0c7",
					click:function(){
						console.log(editor.getText());
					}
				}
			}
	});
```  
	
参数：  
width：编辑器的宽  
height：编辑器的高  
buttons：工具栏图标  

