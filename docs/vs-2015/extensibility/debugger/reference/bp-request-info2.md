---
title: "BP_REQUEST_INFO2 | Microsoft Docs"
ms.custom: ""
ms.date: 11/15/2016
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "BP_REQUEST_INFO2"
helpviewer_keywords: 
  - "BP_REQUEST_INFO2 structure"
ms.assetid: 008c87f7-a76e-43d3-8904-11b225d6a9a5
caps.latest.revision: 10
ms.author: "gregvanl"
manager: "ghogen"
---
# BP_REQUEST_INFO2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Contains the information required to implement a breakpoint, including vendor GUID, constraint and tracepoint.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_REQUEST_INFO2 {  
   BPREQI_FIELDS   dwFields;  
   GUID            guidLanguage;  
   BP_LOCATION     bpLocation;  
   IDebugProgram2* pProgram;  
   BSTR            bstrProgramName;  
   IDebugThread2*  pThread;  
   BSTR            bstrThreadName;  
   BP_CONDITION    bpCondition;  
   BP_PASSCOUNT    bpPassCount;  
   BP_FLAGS        dwFlags;  
   GUID            guidVendor;  
   BSTR            bstrConstraint;  
   BSTR            bstrTracepoint;  
} BP_REQUEST_INFO2;  
```  
  
```csharp  
public struct BP_REQUEST_INFO2 {  
   public uint           dwFields;  
   public Guid           guidLanguage;  
   public BP_LOCATION    bpLocation;  
   public IDebugProgram2 pProgram;  
   public string         bstrProgramName;  
   public IDebugThread2  pThread;  
   public string         bstrThreadName;  
   public BP_CONDITION   bpCondition;  
   public BP_PASSCOUNT   bpPassCount;  
   public uint           dwFlags;  
   public Guid           guidVendor;  
   public string         bstrConstraint;  
   public string         bstrTracepoint;  
};  
```  
  
## Members  
 `dwFields`  
 A combination of flags from the [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md) enumeration that specifies which fields are filled out.  
  
 `guidLanguage`  
 The language GUID.  
  
 `bpLocation`  
 The [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) structure that specifies the type of the breakpoint location.  
  
 `pProgram`  
 The [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) object that represents the application in which the breakpoint occurs.  
  
 `bstrProgramName`  
 The name of the application in which the breakpoint occurs.  
  
 `pThread`  
 The [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) object that represents the thread in which the breakpoint occurs.  
  
 `bstrThreadName`  
 The name of the thread in which the breakpoint occurs.  
  
 `bpCondition`  
 The [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) structure that describes the conditions under which the breakpoint will fire.  
  
 `bpPassCount`  
 The [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md) structure that contains the pass count information of the breakpoint.  
  
 `dwFlags`  
 A combination of flags from the [BP_FLAGS](../../../extensibility/debugger/reference/bp-flags.md) enumeration that specifies the flags for the requested breakpoint.  
  
 `guidVendor`  
 GUID of vendor. May be a null value.  
  
 `bstrConstraint`  
 Name of breakpoint constraint. May be a null value.  
  
 `bstrTracepoint`  
 Name of trace point. May be a null value.  
  
## Remarks  
 This structure is returned by the [GetRequestInfo2](../../../extensibility/debugger/reference/idebugbreakpointrequest3-getrequestinfo2.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetRequestInfo2](../../../extensibility/debugger/reference/idebugbreakpointrequest3-getrequestinfo2.md)   
 [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md)   
 [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)   
 [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)   
 [BP_FLAGS](../../../extensibility/debugger/reference/bp-flags.md)
