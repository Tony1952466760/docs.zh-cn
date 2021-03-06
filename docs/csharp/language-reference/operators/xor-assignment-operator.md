---
title: "^= 运算符（C# 参考） | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.technology: 
  - "devlang-csharp"
ms.topic: "article"
f1_keywords: 
  - "^=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "^= 运算符 [C#]"
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
caps.latest.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
caps.handback.revision: 16
---
# ^= 运算符（C# 参考）
“异或”赋值运算符。  
  
## 备注  
 下列形式的表达式  
  
```  
x ^= y  
```  
  
 按如下规则计算：  
  
```  
x = x ^ y  
```  
  
 不同的是 `x` 只计算一次。  [^ 运算符](../../../csharp/language-reference/operators/xor-operator.md)对整数操作数执行按位“异或”运算，对 [bool](../../../csharp/language-reference/keywords/bool.md) 操作数执行逻辑“异或”运算。  
  
 不能直接重载 ^\=  运算符，但用户定义的类型可重载 [^ operator](../../../csharp/language-reference/operators/xor-operator.md)（请参见 [operator](../../../csharp/language-reference/keywords/operator.md)）。  
  
## 示例  
 [!code-cs[csRefOperators#23](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-assignment-operator_1.cs)]  
  
## 请参阅  
 [C\# 参考](../../../csharp/language-reference/index.md)   
 [C\# 编程指南](../../../csharp/programming-guide/index.md)   
 [C\# 运算符](../../../csharp/language-reference/operators/index.md)