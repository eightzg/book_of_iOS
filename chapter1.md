### 移除控制器的view

> #### 移除控制器的view在viewDidAppear中

```
//只要控件有父控制器，就能移除。
- (void)viewDidAppear:(BOOL)animated {
    [super viewDidAppear:animated];
    [self.view removeFromSuperview];
}
```



