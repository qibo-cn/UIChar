# SwiftUI 多页面

NavigationView 一个带路由效果的容器

NavigationLink 配合NavigationView，包括需要路由的控件，destination属性设置路由目标

```swift
NavigationView{
  List(landmarkData){ landmark in
    NavigationLink(destination: LandmarkDetail(landmark: landmark)){  // destination属性定义目标路由
      LandmarkRow(landmark: landmark)  // 点击该控件，跳转至destination 
    }
  }
  .navigationBarTitle(Text("Landmarks"))  // List标题
}

```

## push方法

```swift
self.navigationController?.pushViewController(viewC, animated: true);
```
## pop方法

### 返回到上一视图

```swift
self.navigationController?.popViewControllerAnimated(true);
```

### 返回到根视图
```swift
self.navigationController?.popToRootViewControllerAnimated(true);
```

### 返回到指定视图
```swift
let viewAarray = self.navigationController?.viewControllers;
self.navigationController?.popToViewController(viewAarray![2], animated: true);
```