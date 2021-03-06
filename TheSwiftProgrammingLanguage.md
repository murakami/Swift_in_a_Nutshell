# プログラミング言語Swift
## サンプルコード
ファイル名: hello.swift

    #!/usr/bin/env xcrun swift

    print("Hello, World!")

コマンド実行

    $ chmod +x hello.swift
    $ ./hello.swift
    Hello, World!

## 基本的な特徴
### 注釈

~~~swift
// 注釈
~~~

---

~~~swift
/* 注釈 */
~~~

### セミコロン
構文を分けるのに利用する。

~~~swift
x = 1; y = 2
~~~

### 空白
字句を分けるなどで利用する。

~~~swift
x=1
y = 2
~~~

### モジュール

~~~swift
import Cocoa
import Foundation.NSDate
import func Darwin.sqrt
~~~

## 型

|名前|内容|
|:--|:--|
|Bool|真偽値 (true, false)|
|Int|符号あり整数型|
|UInt|符号なし整数型|
|Float|単精度(32bit)浮動小数点|
|Double|倍精度(64bit)浮動小数点｜
|Character|Unicode文字|
|String|文字列|
|Int8|符号あり8bit整数型|
|UInt8|符号なし8bit整数型|
|Int16|符号あり16bit整数型|
|UInt16|符号あり16bit整数型|
|Int32|符号あり32bit整数型|
|UInt32|符号なし32bit整数型|
|Int64|符号あり64bit整数型|
|UInt64|符号なし64bit整数型|

### 数値

|接頭語|説明|例|
|:--|:--|:--|
|-|10進数|256, 1024, 3.14, 1.7e2|
|0b|2進数|0b10001011|
|0o|8進数|0o0317|
|0x|16進数|0xEF27|

~~~swift
2.7e4
0x10.4p2
1_123_123
~~~

### 文字と文字列

```swift
let c: Character = "A"
let s: String = "Hello, World!"
```

### 付属型

~~~swift
typealias Byte = UInt8
var b: byte = 64
~~~

### ネスト型

~~~swift
class A {
    enum Kind {
        case First, Second
    }
}

vat n = A.Kind.Second
~~~

## 変数と定数

~~~swift
var n: Int = 123
let pie: Float = 3.14
~~~

### 計算型変数

~~~swift
var str: String
var name: String {
    get {
        return str
    }
    set(name) {
        str = name
    }
}
~~~

### Variable Observers

~~~swift
var count = 0
var value: Int {
    willSet {
        ++count
    }
    didSet {
        print("\(count) \(value)")
    }
}
~~~

## タプル

~~~swift
let value = ("hello", 123, 456)
~~~

~~~swift
func demo() -> (Int, Float) {
    return (789, 3.14)
}
~~~

## 演算子

### 算術演算子

|||
|:--|:--|
|+|加算|
|-|減算|
|*|乗算|
|/|除算|
|++|インクリメント|
|--|デクリメント|

### ビット演算子

||||
|:--|:--|:--|
|~|~A|ビット否定|
|&|A&B|ビット積|
|\||A\|B|ビット和|
|^|A^B|ビット排他的論理和|
|<<|A<<B|左シフト|
|>>|A>>B|右シフト|

### 代入演算子

|||
|:--|:--|
|=|代入|
|+=|加算代入|
|-=|減算代入|
|*=|乗算代入|
|/=|除算代入|
|%=|剰余代入|
|<<=|左シフト代入|
|>>=|右シフト代入|
|&=|ビット積代入|
|\|=|ビット和代入|
|^=|ビット排他的論理和代入|

### 比較演算子

||||
|:--|:--|:--|
|==|A==B|等価|
|!=|A==B|非等価|
|===|A===B|完全等価|
|!==|A!==B|完全非等価|
|<|A<B|小なり|
|<=|A<=B|小なりイコール|
|>|A>B|大なり|
|>=|A>=B|大なりイコール|
|~=|A~=B|パターン照合|

### 論理演算子

||||
|:--|:--|:--|
|!|!A|論理否定|
|&&|A&&B|論理|
|\|\||A\|\|B|論理和|

### オーバーフロー演算子

|||
|:--|:--|
|&+|オーバーフロー加算|
|&-|オーバーフロー減算|
|&*|オーバーフロー乗算|
|&/|オーバーフロー除算|
|&%|オーバーフロー剰余|

### 型キャスト演算子

|||
|:--|:--|
|is|型検証|
|as|キャスト演算子|
|as?|オプショナル型へのキャスト演算子|

## 文字と文字列

~~~swift
var str: String = "hello"
var ch: Character = "A"
let s = "Hello" + ", World"
~~~

## 配列

~~~swift
let array1 = Int[5]
var array2 = [Int]()
var array3 = [Int](count: 3, repeatedValue: 0)
var array4: [Int] = [1, 2, 3, 4, 5]
~~~

~~~swift
let n = array4[1]
let array5 = array4[1...3]
for n in array4 {
    print(n)
}
~~~

## 辞書

~~~swift
var dict1 = [String: String]()
let dict2: [String: String] = ["aaa":"AAA", "bbb":"BBB", "ccc":"CCC"]
for (k, v) in dict2 {
    print(k)
    print(v)
}
~~~

## 関数

~~~swift
func sum(n: Int, o: Int) -> Int {
    return n + o
}

let result = sum(3, 5)
~~~

## クロージャ

~~~swift
let block = {
    (n: Int, o: Int) -> Int in
    return n + o
}

let result = block(3, 5)
~~~

## オプショナル型

~~~swift
var strOpt: String?

if let strConst = strOpt {
    print(strConst)
}
~~~

## 制御構文

~~~swift
for var n = 0; n < 10; n++ {
    print("\(n)")
}

let array = ["Classic", "PowerBook", "MacBook"]
for item in array {
    print(item)
}

var n = 0
while (n < 10) {
    print("\(n)")
    n++
}

var n = 0
do {
    print("\(n)")
    n++
} while (n < 10)

if condition {
}
else if condition {
}
else {
}

switch expression {
    case valueSequence:
        statements
    case valueSequence, valueSequence:
        statements
    default:
        statements
}
~~~

## クラス

~~~swift
class Base {
}

class Demo: Base {
    var instVal: Int = 0

    var propVal: Int {
        get {
            return instVal
        }
        set(val) {
            instVal = val
        }
    }

    init(val: Int) {
        self.instVal = val
    }

    deinit {
    }

    func sum(n: Int) -> Int {
        return instVal + n
    }
}

let demo = Demo(123)
~~~

## 構造体

~~~swift
struct Rect {
    var x = 0.0
    var y = 0.0
    var width = 0.0
    var height = 0.0

    func area() -> Double {
        return width * height
    }

    mutating func resize(scale: Double) {
        width *= scale
        height *= scale
    }
}

let rect = Rect(x:1.0, y:2.0, width:10.0, height:20.0)
~~~

## 列挙型

~~~swift
enum TravelKind {
    case First
    case Business
    case Economy
}
~~~

## アクセス制御

* public
* internal
* private

## 拡張

~~~swift
extension String {
    init(v: MyType) {
        ...
    }

    var length: Int {
        return self.characters.count
    }

    func dbgmsg() {
        print(self)
    }
}
~~~

## 型チェンジとキャスト

~~~swift
var array = [Any]()
array.append(1)
array.append(3.14)
array.append("abcdefg")
~~~

~~~swift
if s is String {
    print("s is string.")
}
~~~

as演算子はインスタンスをキャストする。

~~~swift
let t = s as String
~~~

as?演算子はキャストできない場合はnilを返す。なので、返す値はオプショナル型となる。

~~~swift
let t = s as? String
~~~

as!演算子はキャストできない場合は実行時エラーとなる。

~~~swift
let t = s as! String
~~~

## プロトコル

~~~swift
protocol Playable {
    func play()
    func stop()
}

class Song : Playable {
    func play() {
    }

    func stop() {
    }
}
~~~

## メモリ管理

~~~swift
var s: String? = nil
do {
    let t = "abcdefg"
    s = t
}
print(s ?? "nil")
~~~

~~~swift
weak var s: NSString? = nil
do {
    let t: NSString? = "abcdefg"
    s = t
}
print(s ?? "nil")
~~~

## 総称型

~~~swift
func swap<T>(_ a: inout T, _ b: input T) {
    let temp = a
    a = b
    b = temp
}
~~~

## 演算子の多重定義

~~~swift
func + ([inout] left: Int, right: Int) -> Int {
}
~~~

## Ranges, Intervals, and Strides

~~~swift
A..<B    A<=x<B
A...B    A<=x<=B
~~~

~~~swift
var i = 1.1...2.2
i.start
i.end
i.contains(1.6)
~~~

~~~swift
for x in stride(from:0, to:20, by:2) {
}
~~~

## グローバル関数

~~~swift
advancedBy(n: Distance)
~~~