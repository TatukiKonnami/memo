# 定義情報
## 型情報
### 型情報(type)
| 型 | 中間コード | 備考 |
|:-:|:-:|:-:|
| integer | i32 |  |
| double | double |  |
| void | void | |
| char | | |
| float | | |

### 拡張型情報 (expand_type extent type as type)
| 型 | 中間コード | 備考 |
|:-:|:-:|:-:|
| pointer | `<type> *` |  |
| array | `[ <elements> × <type> ]` |  |

## 型システム
### function type
```<returntype> (<parameter list>)```

## 演算子情報
### 演算子
| 演算子 | 中間コード | 備考 |
|:-:|:-:|:-:|
| add | add | |
| sub | sub |  |
| mul |  | |
| div |  | |

