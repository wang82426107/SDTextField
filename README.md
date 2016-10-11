# SDTextField
诱导输入的输入框
</br>
####SDTextField的快速集成
***

SDTextField使用起来也是比较简单.我们只需要简简单单的两三步就能快速创建SDTextField对象.首先把SDTextFieldDemo中SDTextField.h和SDTextField.m文件拖到你的工程中.
![](http://upload-images.jianshu.io/upload_images/1396375-c8368cf6270b3885.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

然后使用**+(instancetype)initWithFrame:(CGRect)frame;**创建即可.创建完成之后,我们还需要配置诱导输入查询库数组,然后添加即可.整体代码如下.

```
    self.textField = [SDTextField initWithFrame:CGRectMake(75, 100, 250, 35)];
    
    self.textField.dataArray = [NSMutableArray arrayWithArray:@[@"a",@"ab",@"A",@"c",@"admin"]];
    
    [self.view addSubview:self.textField];
    
```

唯一值得注意的,就是高度问题.诱导输入列表的的高度将会是textfield的三倍,如果你需要让列表高度更高或者更低,请自行修改**heightMultiple**,这个属性将会影响两者的高度比例.用法如下所示.
```
    self.textField.heightMultiple = 5;

```
