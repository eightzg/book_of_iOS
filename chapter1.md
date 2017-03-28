### 移除控制器的view

> #### 移除控制器的view在viewDidAppear中

```
//只要控件有父控制器，就能移除。
- (void)viewDidAppear:(BOOL)animated {
    [super viewDidAppear:animated];
    [self.view removeFromSuperview];
}
```

### UILabel的使用

> #### UILabel的使用

```
    // 1.1 创建UILabel对象
    UILabel *label = [[UILabel alloc] init];

    // 1.2 设置frame
    label.frame = CGRectMake(100, 100, 202, 175);

    // 1.3 设置背景颜色
    label.backgroundColor = [UIColor redColor];

    // 1.4 设置文字
    label.text = @"da shen 11期最牛逼!!!!da shen da shen da shen da shen da shen ";

    // 1.5 居中
    label.textAlignment = NSTextAlignmentCenter;

    // 1.6 设置字体大小
    label.font = [UIFont systemFontOfSize:20.f];
    label.font = [UIFont boldSystemFontOfSize:25.f];
    label.font = [UIFont italicSystemFontOfSize:20.f];

    // 1.7 设置文字的颜色
    label.textColor = [UIColor whiteColor];

    // 1.8 设置阴影(默认是有值)
    label.shadowColor = [UIColor blackColor];
    label.shadowOffset = CGSizeMake(-2, 1);

    // 1.9 设置行数(0:自动换行)
    label.numberOfLines = 1;

    // 1.10 显示模式
    label.lineBreakMode =  NSLineBreakByTruncatingHead;

    /*
     NSLineBreakByWordWrapping = 0,  // 单词包裹,换行的时候会以一个单词换行
     NSLineBreakByCharWrapping,        // 字符包裹换行,换行的时候会以一个字符换行
     NSLineBreakByClipping,        // 裁剪超出的内容
     NSLineBreakByTruncatingHead,    // 一行中头部省略(注意:numberOfLines要为1): "...wxyz"
     NSLineBreakByTruncatingTail,    // 一行中尾部省略: "abcd..."
     NSLineBreakByTruncatingMiddle    // 一行中中间部省略:  "ab...yz"
     */
```

### 图片设置毛玻璃效果

```
    // 6.加毛玻璃

    // 6.1 创建UIToolBar对象
    UIToolbar *toolBar = [[UIToolbar alloc] init];
    // 6.2 设置toolBar的frame
    toolBar.frame = imageView.bounds;
    // 6.3 设置毛玻璃的样式
    toolBar.barStyle = UIBarStyleBlack;
    toolBar.alpha = 0.01;
    // 6.4 加到imageView中
    [imageView addSubview:toolBar];
```

### 图片加载的两种方式

> #### 1.imageNamed
>
> #### 2.imageWithContentOfFile:

```
   1. 加载Assets.xcassets这里面的图片:
    1> 打包后变成Assets.car
    2> 拿不到路径
    3> 只能通过imageNamed:来加载图片
    4> 不能通过imageWithContentsOfFile:来加载图片
 
   2. 放到项目中的图片:
    1> 可以拿到路径
    2> 能通过imageNamed:来加载图片
    3> 也能通过imageWithContentsOfFile:来加载图片
```



