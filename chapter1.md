### 移除控制器的view

> #### 移除控制器的view在viewDidAppear中

```
- (void)viewDidAppear:(BOOL)animated {
    [super viewDidAppear:animated];
    [self.view removeFromSuperview];
}
```



