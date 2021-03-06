---
title: "如何：在 Visual Basic 中记录异常 | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: ".net"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "异常, 日志记录"
  - "异常, 跟踪"
ms.assetid: a26c60e2-ae39-444a-aebb-33eccadc0eeb
caps.latest.revision: 19
author: "stevehoag"
ms.author: "shoag"
caps.handback.revision: 19
---
# 如何：在 Visual Basic 中记录异常
[!INCLUDE[vs2017banner](../../../../visual-basic/includes/vs2017banner.md)]

可以使用记录信息的 `My.Application.Log` 和 `My.Log` 对象提供有关在应用程序中发生的异常。  这些示例演示如何使用 `My.Application.Log.WriteException` 方法添加到您显式捕获的记录未经处理的异常和异常。  
  
 若要记录跟踪信息，请使用 `My.Application.Log.WriteEntry` 方法。  有关更多信息，请参见 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>  
  
### 记录已处理的异常  
  
1.  创建将生成异常信息的方法。  
  
     [!code-vb[VbVbalrMyApplicationLog#9](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_1.vb)]  
  
2.  使用 `Try...Catch` 块捕获异常。  
  
     [!code-vb[VbVbalrMyApplicationLog#6](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_2.vb)]  
  
3.  将可能发生在 `Try` 的异常块中的代码。  
  
     取消注释 <xref:System.NullReferenceException> 导致异常的 `Dim` 和 `MsgBox` 行。  
  
     [!code-vb[VbVbalrMyApplicationLog#7](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_3.vb)]  
  
4.  在 `Catch` 块，使用 `My.Application.Log.WriteException` 方法写入异常信息。  
  
     [!code-vb[VbVbalrMyApplicationLog#8](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_4.vb)]  
  
     下面的示例演示用于记录已处理异常的完整代码。  
  
     [!code-vb[VbVbalrMyApplicationLog#10](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_5.vb)]  
  
### 记录未经处理的异常  
  
1.  在中选择一个项目。在 **解决方案资源管理器**。  在 **项目** 菜单中，选择 **属性**。  
  
2.  单击 **应用程序** 选项。  
  
3.  单击 **查看应用程序事件** 按钮打开代码编辑器。  
  
     将打开 ApplicationEvents.vb 文件。  
  
4.  保持 ApplicationEvents.vb 的文件将在代码编辑器中。  在 **常规** 菜单中，选择 **MyApplication 事件**。  
  
5.  在 **声明** 菜单中，选择 **UnhandledException**。  
  
     ，在主应用程序运行之前，应用程序将引发 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException> 事件。  
  
6.  添加 `My.Application.Log.WriteException` 方法。 `UnhandledException` 事件处理程序。  
  
     [!code-vb[VbVbalrMyApplicationLog#4](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_6.vb)]  
  
     下面的示例演示记录未经处理的异常的完整代码。  
  
     [!code-vb[VbVbalrMyApplicationLog#5](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_7.vb)]  
  
## 请参阅  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>   
 [使用 Application 日志](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)   
 [如何：编写日志消息](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-log-messages.md)   
 [演练：确定 My.Application.Log 写入信息的位置](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)   
 [演练：更改 My.Application.Log 写入信息的位置](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)