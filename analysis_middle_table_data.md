# 定義情報
## 型情報
### 型情報(type)
| 型 | 中間コード | 備考 |
|:-:|:-:|:-:|
| integer | i32 |  |
| double | double |  |
| void | void | |
| char | i8 | |
| float | float | |

### 拡張型情報 (expand_type extent type as type)
| 型 | 中間コード | 備考 |
|:-:|:-:|:-:|
| pointer | `<type> *` |  |
| array | `[ <elements> × <type> ]` |  |
| structure | ` %mytype = <type> { <type list> }   ` | |
| opaque | `%mytype = <type> opaque` | 未定義な構造体 |

## 型システム
### function type
```<returntype> (<parameter list>)```

## 演算子情報
### 演算子
| 演算子 | 中間コード | 備考 |
|:-:|:-:|:-:|
| add | add | |
| sub | sub |  |
| mul | mul | |
| div | sdiv | |
| rem | srem | |

### 演算
```  <operator> <type> <type> <registar> ```

## 終端命令
### 終端命令
| 終端命令 | 中間コード | 備考 |
|:-:|:-:|:-:|
| ret | `ret <type> <value>` | |
| br | `br i1 <cond>, label <iftrue>, label <iffalse>` | |
| switch | `switch <intty> <value>, label <defaultdest> [ <intty> <val>, label <dest> ... ]` | |

# AST block
## ループ命令
- WhileStmt
- ForStmt
