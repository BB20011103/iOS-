# 作业1
## 1.按顺序打印出App、ViewController生命周期的各个事件
### (1)App生命周期：
```
点击程序图标->执行main函数->通过UIApplicationMain函数->初始化UIApplication对象并且为他设置代理对象->UIApplication对象->（监听系统事件）程序结束退出
```
### (2)ViewController生命周期：
```
alloc/init(初始化)->loadView->viewDidLoad->viewWillAppear->viewDidAppear->viewDidDisappear->viewDidDisappear->dealloc
```
## 2.写出五种常用的 UI 控件
``` 
UIScrollView
UITableView
UICollectionView
UIWebView
WKWebView
```
## 3.列举出三个 UITableViewDelegate 声明的方法
### (1)选中某行cell调用
```
- (void)tableView:(UITableView *)tableView didSelectRowAtIndexPath:(NSIndexPath *)indexPath
```
### (2)自定义每组头部的view需要使用UITableViewHeaderFooterView
```
- (UIView *)tableView:(UITableView *)tableView viewForHeaderInSection:(NSInteger)section; 
```
### (3)自定义每组尾部的view
```
- (UIView *)tableView:(UITableView *)tableView viewForFooterInSection:(NSInteger)section;
```
