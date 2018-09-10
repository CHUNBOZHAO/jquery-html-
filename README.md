# jquery-html-
html两个表单数据联动
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <script src="http://libs.baidu.com/jquery/1.8.3/jquery.min.js"></script>
    <title></title>
</head>
<body>
<input id="txt" type="text">
<input id="txt1" type="text">
<script>
        var flag = true;
        $('#txt').on('compositionstart',function(){
            flag = false;
        })
        $('#txt').on('compositionend',function(){
            flag = true;
        })
        $('#txt').on('input',function(){
            var _this = this;
            setTimeout(function(){

                if(flag){//TODO:添加事件

                    <!--alert($(_this).val())-->
                    console.log($(_this).val());
                    document.getElementById("txt1").value=$(_this).val()
                }
            },0)
        })
    </script>
</body>
</html>
