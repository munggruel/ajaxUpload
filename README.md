
13KB 兼容IE6以上浏览器，chrome，firefox，手机浏览器 jquery 插件ajax文件上传，
对于不支持ajax form data上传的IE8和IE8以下浏览器通过不可见的iframe模拟ajax提交

########图片上传#########
$(formId + selector).ajaxFileUpload({
        width: 1000,
        url: 'upload.php',
        onChange: function (filename) {
            alert("上传文件名是"+filename);
        },
        onSubmit: function (filename) {
            alert("正在提交"+filename);
        },
        onProgress: function (percentComplete) {
            alert("已上传：" + percentComplete + "%");
        },
        onComplete: function (response, filename, base64) {
			//response 是服务端返回的消息
            alert("上传图片的base64编码（IE8以上浏览器有效）"+ base64);
        },
        onError: function (filename) {
			//错误处理
        }
    });
    
########文件上传#########
$(formId + selector).ajaxFileUpload({
        url: $$.ROOT + 'do-uploadAttach.php',
		onChange: function (filename) {
            alert("上传文件名是"+filename);
        },
        onSubmit: function (filename) {
            alert("正在提交"+filename);
        },
        onComplete: function (response, filename, base64) {
           	//response 是服务端返回的消息
            alert("上传图片的base64编码（当是图片文件时 IE8以上浏览器有效）"+ base64);
        },
        onError: function (filename) {
			//错误处理
        }
    });
