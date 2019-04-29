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
  
Ruft eine benutzerdefinierte Funktion in einer Hochleistungs-Computing-Umgebung auf.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parameter

_SessionId_
  
> Die ID der Sitzung, in der der Anruf vorgenommen werden soll.
    
_XLLName_
  
> Der Name der XLL, die die benutzerdefinierte Funktion enthält.
    
_UDFName_
  
> Der Name der benutzerdefinierten Funktion.
    
_CallBackAddr_
  
> Die Funktion, die der Connector aufrufen sollte, wenn die benutzerdefinierte Funktion abgeschlossen ist.
    
_pxAsyncHandle_
  
> Das von Excel verwendete asynchrone Handle und der Konnektor zum Nachverfolgen des ausstehenden benutzerdefinierten Funktionsaufrufs. Der Connector verwendet ihn später, wenn der Anruf beendet wird, wenn er mit dem Funktionszeiger, der im _CallBackAddr_ -Argument übergeben wird, zurück in Excel aufruft. 
    
_ArgCount_
  
> Die Anzahl der Argumente, die an die benutzerdefinierte Funktion übergeben werden sollen. Der maximal zulässige Wert ist 255.
    
_Parameter1_
  
> Ein Wert, der an die benutzerdefinierte Funktion weitergegeben werden soll. Wiederholen Sie dieses Argument für jeden von _ArgCount_angegebenen Parameter.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess** , wenn der UDF-Aufruf erfolgreich initiiert wurde; **xlHpcRetInvalidSessionId** , wenn das _SessionID_ -Argument ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern, einschließlich Timeout. Wenn der Aufruf einen Fehlercode (alles außer **xlHpcRetSuccess**) zurückgibt, sieht Excel, dass der UDF-Aufruf fehlgeschlagen ist, die _pxAsyncHandle_ungültig macht und nicht erwartet, dass ein Rückruf stattfindet.
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion wird asynchron ausgeführt.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

