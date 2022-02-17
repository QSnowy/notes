## swift
类和结构体
- 类可继承，属于类型引用；结构体属于值类型，与`Int`等基本数据类型一样

## 泛型
### 泛型函数
类型占位符 `T`，函数不使用固定类型的参数，增大灵活性
```Swift
func swapTwoValues<T>(_ a: inout T, _ b: inout T) {}
```
### 泛型类型
定义一个泛型栈结构体，类型占位符 `Element`
```Swift
struct Stack<Element> {
    var items: [Element] = []
    mutating func push(_ item: Element) {
        items.append(item)
    }
    mutating func pop() -> Element {
        return items.removeLast()
    }
}
```

### 泛型约束
在类型名后放置一个类名或者协议名，标识该类型属于某个类型或遵守某个协议

```Swift
func someFoo<T: SomeClass, U: SomeProtocol>(someT: T, someU: U) {
    
}
```