# baidu-ife


stage-1 task-3
三行布局有两种方法清除浮动来

第一种 clear 

Nicolas Gallagher 在A new micro clearfix hack中提供了一种看起来更清爽的做法

.floatfix:after{
    content:"";
    display:table;
    clear:both;
}

但是IE6、7不支持伪元素怎们办？这就需要我们使用BFC方法

第二种 使父级元素成为bfc

如何形成BFC

    float为 left|right
    overflow为 hidden|auto|scroll
    display为 table-cell|table-caption|inline-block
    position为 absolute|fixed


关于 box-sizing
当你设置一个元素为 box-sizing: border-box; 时，此元素的内边距和边框不再会增加它的宽度。 
