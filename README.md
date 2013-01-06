jquery-image-map
================

jQuery图片热点链接添加编辑插件

### 使用

	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
	<html xmlns="http://www.w3.org/1999/xhtml">
	<head>
		<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
		<title>Image Maps test</title>
		<script type="text/javascript" language="javascript" src="javascript/jquery-1.4.2.min.js"></script>
		<script type="text/javascript" language="javascript" src="javascript/jquery.image-maps.js"></script>
		<script type="text/javascript" language="javascript">
		$(function(){
			$('#imgMap').imageMaps();
		});
		</script>
	</head>
	<body>
		<div id="imgMap">
			<img src="womanExercise150.jpg" name="test" width="417" height="264" border="0" usemap="#Map" ref='imageMaps' />
			<map name="Map">
				<area shape="rect" coords="203,134,383,187" href="http://yiye.name" />
			</map>
		</div>
	</body>
	</html>

### 使用说明:

<div id="imgMap">为整个编辑功能的容器，其中包括两个部分：

- 1、img标签，当然这个img标签外层你可以再嵌套其他的标签，值得注意的是ref='imageMaps'这个属性，这是必需的，不然程序将忽略掉这个图片。

- 2、map标签，name属性与img标签的usemap属性对应起来，这个标签包含初始化时这个图片具有的热点链接。

    // 绑定插件功能
    $('#imgMap').imageMaps();