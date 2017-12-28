# 定義情報
## コメント
```; <string>```

## レジスタ
``` %<NUM> ```
レジスタにはあたいを保持できる

## メモリ
### メモリ割り当て
```alloc <type>, align <byte>```
alignは指定したバイト数でアラインメント｡ 領域が確保できない時の挙動は未定義
### メモリ書き出し
``` store <type> <NUM>, <type> <registar>```

## 型情報
### 型情報(type)
| 型 | 中間コード | 備考 |
|:-:|:-:|:-:|
| integer | i32 |  |
| double | double |  |
| void | void | |
| char | i8 | |
| float | float | |
| long | i64| |

### 拡張型情報 (expand_type extent type as type)
| 型 | 中間コード | 備考 |
|:-:|:-:|:-:|
| pointer | `<type> *` |  |
| array | `[ <elements> × <type> ]` |  |
| structure | ` %mytype = <type> { <type list> }   ` | |
| opaque | `%mytype = <type> opaque` | 未定義な構造体(前方宣言) |
| function | ` %mytype = <returntype> (<parameter list>) ` | |

## 型システム
### function type
```<returntype> (<parameter list>)```

## 演算子情報
### 演算子
| 演算子 | 中間コード | 備考 |
|:-:|:-:|:-:|
| add | ```result = add < \| nuw \| nsw > <type> <op1>, <op2> ``` | <op1><op2>は値 |
| fadd | `result = fadd <type> <op1>, <op2>` | <op1><op2>は値 |
| sub | `result = sub < \| nuw \| nsw > <type> <op1>, <op2>` |  |
| fsub | `result = fsub  <type> <op1>, <op2>` |  |
| mul | `result = mul < \| nuw \| nsw > <type> <op1>, <op2>` | |
| fmul | `result = fmul <type> <op1>, <op2>` | |
| udiv | `result = udiv < \| exact > <type> <op1>, <op2>` | |
| sdiv | `result = sdiv < \| exact > <type> <op1>, <op2>` | |
| fdiv | `result = fdiv  <type> <op1>, <op2>` |  |
| urem | `result = urem  <type> <op1>, <op2>` | |
| srem | `result = srem  <type> <op1>, <op2>` | |
| frem | `result = frem  <type> <op1>, <op2>` | |
| shl | `result = shl < \| nuw \| nsw > <type> <op1>, <op2>` | 左シフト |
| lshr | `result = lshr < \| exact > <type> <op1>, <op2>` | 論理右シフト |
| ashr | `result = lshr < \| exact > <type> <op1>, <op2>` | 算術右シフト |
| and | `result = and <type> <op1>, <op2>` | 論理積 |
| or | `result = or <type> <op1>, <op2>` | 論理和 |
| xor | `result = xor <type> <op1>, <op2>` | 排他的論理和 |

### 演算
``` result =  <operator> < | nuw | nsw | exact> <type> <type> <registar> ```

## メモリアクセス
| 命令 | 中間コード | 備考 |
|:-:|:-:|:-:|
| alloca | 'result = alloca <type> [, <type> <NumElements>] [, align <alignment>]' | |
| load | 'result = load <type> <type>* <registar> [, align <alignment>]' | |
| store | 'store <type> <value>, <type>* <registar> [, align <alignment>]'| |
| getelementptr | 'result = getelementptr inbounds <type>, <type>* <registar> [, <type> <value>]'| |  


## 終端命令
### 終端命令
| 終端命令 | 中間コード | 備考 |
|:-:|:-:|:-:|
| ret | `ret <type> <value>` | |
| br | `br i1 <cond>, label <iftrue>, label <iffalse>` | |
| switch | `switch <intty> <value>, label <defaultdest> [ <intty> <val>, label <dest> ... ]` | |

## グローバル変数
``` global <type> <value> ```
## Function system

## 最小ブロック
``` label  ```


# AST block
## ループ命令
- WhileStmt
- ForStmt

`Ast勉強wiki参照`

`|-＿-`
