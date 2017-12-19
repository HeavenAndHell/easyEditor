**这只是一个简单的编辑器，拥有插入表情，插入行块功能，支持IE9+**

easyEditor
====================

首先你需要引入css与JS

    <link rel="stylesheet" href="css/easyEditor.css" />
    <script src="js/easyEditor.js"></script>

html你只需要一个div

	<div id="editor" style="width:500px;height:300px;"></div>

我们需要实例化

    var editor = new EasyEditor('editor');
    
插入标签

	/**
     *
     * @param {object} 
     *			src {string} 表情路径 
     *			remark {string} 表情说明
     *			afterInsert {function} 插入后的回调函数
     *
     *
     * @return {object} editor Object
     */
    
    editor.insertEmoji({
		src : 'emoji/1.gif', 
		remark : '笑脸',
		afterInsert : function(){
			
		}
	});

插入行块

	/**
     * 
     * @param {object} 
	 *		  text {string} 文字 
	 *		  color {string} 文字颜色
	 *		  afterInsert {function} 插入后的回调函数
	 *
	 *
     * @return {object} editor Object
     */
    
    editor.insertEmoji({
		text : '@somebody', 
		color : '#f00',
		afterInsert : function(){
			
		}
	});

获取编辑器里面的html
	
	var myhtml = editor.getContent(false);

获取编辑器里面的text
	
	var mytext = editor.getContent(true);
	
属性
	
	editor.sel; // selection 对象
	editor.ran; // range 对象
	editor.obj; // 编辑器对象(即文中id为editor的div);
	
功能介绍完毕，是不是很简单，如果转载，请标注出处哦，以后会陆续新增功能，多谢关注 Mr.Li
