---
title: C-API-Funktionen, die nur von einer DLL oder XLL aufgerufen werden können
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api called from dll or xll
ms.localizationpriority: medium
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8c53a2f68dab76bc68ea756f25d87e351b8700f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605652"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>C-API-Funktionen, die nur von einer DLL oder XLL aufgerufen werden können

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Die C-API bietet 15 Microsoft Excel Rückruffunktionen, die nur mithilfe der **Funktionen Excel4,** **Excel4v,** **Excel12** oder **Excel12v** aufgerufen werden können (oder durch eine dieser Funktionen indirekt mithilfe der Framework-Funktionen **Excel** oder **Excel12f).** Dies bedeutet, dass sie nur von einer DLL oder XLL aufgerufen werden können.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[xlAbort](xlabort.md)
  
[xlAsyncReturn](xlasyncreturn.md)
  
[xlCoerce](xlcoerce.md)
  
[xlDefineBinaryName](xldefinebinaryname.md)
  
[xlDisableXLMsgs](xldisablexlmsgs.md)
  
[xlEnableXLMsgs](xlenablexlmsgs.md)
  
[xlEventRegister](xleventregister.md)
  
[xlFree](xlfree.md)
  
[xlGetBinaryName](xlgetbinaryname.md)
  
[xlGetHwnd](xlgethwnd.md)
  
[xlGetInst](xlgetinst.md)
  
[xlGetInstPtr](xlgetinstptr.md)
  
[xlGetName](xlgetname.md)
  
[xlRunningOnCluster](xlrunningoncluster.md)
  
[xlSet](xlset.md)
  
[xlSheetId](xlsheetid.md)
  
[xlSheetNm](xlsheetnm.md)
  
[xlStack](xlstack.md)
  
[xlUDF](xludf.md)
  
## <a name="see-also"></a>Siehe auch



[C-API-Rückruffunktionen Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)

