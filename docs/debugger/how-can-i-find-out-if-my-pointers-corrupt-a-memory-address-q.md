---
title: "How Can I Find Out If My Pointers Corrupt a Memory Address? | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
  - "VB"
  - "FSharp"
  - "C++"
helpviewer_keywords: 
  - "addresses, pointers corrupting memory address"
  - "memory, corruption"
  - "pointers, corrupting memory addresses"
  - "memory address corruption by pointers"
  - "debugging [C++], memory corruption"
  - "corrupted memory address"
ms.assetid: a147c939-4fb1-415c-8410-cf303781e9e8
caps.latest.revision: 19
author: "mikejo5000"
ms.author: "mikejo"
manager: ghogen
ms.workload: 
  - "multiple"
---
# How Can I Find Out If My Pointers Corrupt a Memory Address?
## Problem Description  
 I think that one of my pointers may be corrupting memory at address 0x00408000. How can I find out what is happening there?  
  
## Solution  
  
#### Check for heap corruption  
  
-   Most memory corruption is actually due to heap corruption. Try using the Global Flags Utility (gflags.exe) or pageheap.exe. See [http://support.microsoft.com/default.aspx?scid=kb;en-us;286470](http://support.microsoft.com/default.aspx?scid=kb;en-us;286470).  
  
#### To find where the memory address is modified  
  
1.  Set a data breakpoint at 0x00408000. See [Set a data change breakpoint (native C++ only)](../debugger/using-breakpoints.md#BKMK_set_a_data_breakpoint_native_cplusplus_only).  
  
2.  When you hit the breakpoint, use the **Memory** window to view memory contents starting at 0x00408000. For more information, see [Memory Windows](../debugger/memory-windows.md).  
  
## See Also  
 [Debugging Native Code FAQs](../debugger/debugging-native-code-faqs.md)   
 [Debugging Native Code](../debugger/debugging-native-code.md)