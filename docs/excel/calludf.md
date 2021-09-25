---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f02b20c5a8355f68a937ad96cf4106c37f3a767a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614619"
---
# <a name="calludf"></a>CallUDF

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine benutzerdefinierte Funktion in einer hochleistungsfähigen Computerumgebung auf.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parameter

_SessionId_
  
> Die ID der Sitzung, in der der Anruf tätigen wird.
    
_XLLName_
  
> Der Name der XLL, die die benutzerdefinierte Funktion enthält.
    
_UDFName_
  
> Der Name der benutzerdefinierten Funktion.
    
_CallBackAddr_
  
> Die Funktion, die der Connector aufrufen soll, wenn die benutzerdefinierte Funktion abgeschlossen ist.
    
_pxAsyncHandle_
  
> Das asynchrone Handle, das von Excel und dem Connector zum Nachverfolgen des ausstehenden benutzerdefinierten Funktionsaufrufs verwendet wird. Der Connector verwendet ihn später, wenn der Aufruf abgeschlossen ist, wenn er mithilfe des Funktionszeigers, der im _CallBackAddr-Argument_ übergeben wird, zurück in Excel aufruft. 
    
_ArgCount_
  
> Die Anzahl der Argumente, die an die benutzerdefinierte Funktion übergeben werden sollen. Der maximal zulässige Wert ist 255.
    
_Parameter1_
  
> Ein Wert, der an die benutzerdefinierte Funktion übergeben werden soll. Wiederholen Sie dieses Argument für jeden durch  _ArgCount_ angegebenen Parameter.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess,** wenn der UDF-Aufruf erfolgreich initiiert wurde; **xlHpcRetInvalidSessionId,** wenn das _Argument SessionId_ ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern, einschließlich Timeout. Wenn der Aufruf einen Fehlercode zurückgibt (alles außer **xlHpcRetSuccess),** betrachtet Excel den UDF-Aufruf als fehlgeschlagen, macht die _pxAsyncHandle_ ungültig und erwartet keinen Rückruf.
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion wird asynchron ausgeführt.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

