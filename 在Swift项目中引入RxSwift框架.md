# 在Swift项目中引入RxSwift框架

<a name="0k1Qd"></a>
##### 前言
> 首先从GitHub拿到源代码，然后像引入 Alamofire一样，直接拖拽 Rx.xcodeproj。
> 接着将 RxCocoa.framework、RxSwift.framework 库添加入Linked Frameworks and Libraries中。
> 在使用位置的地方导入RxSwift，RxCocoa。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/235650/1557130721327-372e45f6-0681-41ca-9f38-4846956d07a2.png#align=left&display=inline&height=257&name=image.png&originHeight=514&originWidth=1074&size=88912&status=done&width=537)<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/235650/1557130456307-a2ab9212-67e5-4231-9f31-71f29df1ae50.png#align=left&display=inline&height=306&name=image.png&originHeight=612&originWidth=540&size=425233&status=done&width=270)<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/235650/1557130669379-e57f9dbb-5c1a-4b21-af6b-dcb587a24924.png#align=left&display=inline&height=356&name=image.png&originHeight=712&originWidth=1782&size=128810&status=done&width=891)

---
<a name="cW0Rh"></a>
##### 使用
```swift
import UIKit
import RxSwift
import RxCocoa

class ViewController: UIViewController {

    let disposeBag = DisposeBag()
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        let rect = CGRect.init(x: 0, y: 100, width: 200, height: 44)
        let button = UIButton.init(frame: rect)
        button.backgroundColor = UIColor.blue
        button.setTitle("RxSwift", for: .normal)
        self.view.addSubview(button)
        
        button.rx.tap.subscribe(onNext: { () in
            print("hello RxSwift")
        }).disposed(by: disposeBag)
    }
  
}
```

