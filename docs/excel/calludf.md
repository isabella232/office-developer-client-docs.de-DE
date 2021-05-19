---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433011"
---
# <a name="calludf"></a>CallUDF

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine benutzerdefinierte Funktion in einer hochleistungsorientierten Computerumgebung auf.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parameter

_SessionId_
  
> Die ID der Sitzung, in der der Anruf zu nehmen ist.
    
_XLLName_
  
> Der Name der XLL, die die benutzerdefinierte Funktion enthält.
    
_UDFName_
  
> Der Name der benutzerdefinierten Funktion.
    
_CallBackAddr_
  
> Die Funktion, die der Connector aufrufen soll, wenn die benutzerdefinierte Funktion beendet ist.
    
_pxAsyncHandle_
  
> Das asynchrone Handle, das von Excel und dem Connector zum Nachverfolgen des ausstehenden benutzerdefinierten Funktionsaufrufs verwendet wird. Der Connector verwendet ihn später, wenn der Aufruf beendet ist, wenn er mit Excel aufruft, der im _Argument CallBackAddr übergeben_ wird. 
    
_ArgCount_
  
> Die Anzahl der Argumente, die an die benutzerdefinierte Funktion übergeben werden. Der maximal zulässige Wert ist 255.
    
_Parameter1_
  
> Ein Wert, der an die benutzerdefinierte Funktion übergeben werden soll. Wiederholen Sie dieses Argument für jeden parameter, der durch _ArgCount angegeben wird._
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess,** wenn der #A0 erfolgreich initiiert wurde. **xlHpcRetInvalidSessionId,** wenn _das Argument SessionId_ ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern, einschließlich Eines-Zeit-Outs. Wenn der Aufruf Fehlercode zurückgibt (mit Ausnahme von **xlHpcRetSuccess),** wird von Excel der UDF-Aufruf als fehlgeschlagen betrachtet, der _pxAsyncHandle_ ungültig gemacht und kein Rückruf erwartet.
  
## <a name="remarks"></a>Hinweise

Diese Funktion wird asynchron ausgeführt.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

