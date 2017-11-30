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