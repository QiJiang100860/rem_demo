利用rem编写不同分辨率的移动端页面
1.设定视口
<meta name="viewport" content="initial-scale=1,maximum-scale=1, minimum-scale=1">
2.根据设计稿设定html根节点的大小
<script type="text/javascript"> 　　
document.documentElement.style.fontSize = document.documentElement.clientWidth / 750*100 + 'px';
</script>
注：我当前的设计稿是width = 750 根据上面计算1rem = 100px 设当下设计稿中的尺寸为perCule, 计算转换为rem (perCule/100)+rem
3.实际开发在less中设全局变量@r = 100rem 注：@r = 100rem中,单位rem只是为了计算结果后面为rem,100为基数。
4.注意计算出来的rem值，在改变分辨率时，只是根据rem比例去重置整个页面。没有必要纠结@r的值