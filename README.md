13KB ����IE6�����������chrome��firefox���ֻ������ jquery ���ajax�ļ��ϴ���
���ڲ�֧��ajax form data�ϴ���IE8��IE8���������ͨ�����ɼ���iframeģ��ajax�ύ
########ͼƬ�ϴ�#########
$(formId + selector).ajaxFileUpload({
        width: 1000,
        url: 'upload.php',
        onChange: function (filename) {
            alert("�ϴ��ļ�����"+filename);
        },
        onSubmit: function (filename) {
            alert("�����ύ"+filename);
        },
        onProgress: function (percentComplete) {
            alert("���ϴ���" + percentComplete + "%");
        },
        onComplete: function (response, filename, base64) {
			//response �Ƿ���˷��ص���Ϣ
            alert("�ϴ�ͼƬ��base64���루IE8�����������Ч��"+ base64);
        },
        onError: function (filename) {
			//������
        }
    });
########�ļ��ϴ�#########
$(formId + selector).ajaxFileUpload({
        url: $$.ROOT + 'do-uploadAttach.php',
		onChange: function (filename) {
            alert("�ϴ��ļ�����"+filename);
        },
        onSubmit: function (filename) {
            alert("�����ύ"+filename);
        },
        onComplete: function (response, filename, base64) {
           	//response �Ƿ���˷��ص���Ϣ
            alert("�ϴ�ͼƬ��base64���루����ͼƬ�ļ�ʱ IE8�����������Ч��"+ base64);
        },
        onError: function (filename) {
			//������
        }
    });