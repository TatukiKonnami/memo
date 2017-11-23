# 定義情報
## 型情報
### 型情報(type)
| 型 | 中間コード | 抽出の実装 |
|:-:|:-:|:-:|
| integer | i32 | 〇 |
| double | double | 〇 |
| void | void | |
| char | | |
| float | | |

### 拡張型情報 (expand_type extent type as type)
| 型 | 中間コード | 抽出の実装 |
|:-:|:-:|:-:|
| pointer | `<type> *` | ○ |
| array | `[ num × <type> ]` |  |

## 型システム
### function type
```<returntype> (<parameter list>)```

## 演算子情報
### 演算子
| 演算子 | 中間コード | 抽出の実装 |
|:-:|:-:|:-:|
| add | + | |
| sub | - |  |
| mul | * | |
| div | / | |

