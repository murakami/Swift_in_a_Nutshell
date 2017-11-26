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

## タプル

## 演算子

## 文字と文字列

## 配列

## 辞書

## 関数

## クロージャ

## オプショナル型

## 制御構文

## クラス

## 構造体

## 列挙型

## アクセス制御

## 拡張

## 型チェンジとキャスト

## プロトコル

## メモリ管理

## 総称型

## 演算子の多重定義

## Ranges, Intervals, and Strides

## グローバル関数