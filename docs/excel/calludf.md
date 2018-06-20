---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790384"
---
# <a name="calludf"></a>CallUDF

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine benutzerdefinierte Funktion in einer High Performance computing-Umgebung.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parameter

_Sitzungs-ID_
  
> Die ID der Sitzung in dem, den Anruf zu tätigen.
    
_XLLName_
  
> Der Name der XLL, die die benutzerdefinierte Funktion enthält.
    
_UDFName_
  
> Der Name der benutzerdefinierten Funktion.
    
_CallBackAddr_
  
> Die Funktion, die der Connector aufrufen soll, wenn die benutzerdefinierte Funktion abgeschlossen ist.
    
_pxAsyncHandle_
  
> Die asynchrone Handle von Excel und den Connector zur Verfolgung des ausstehenden Funktionsaufrufs verwendet. Der Connector später verwendet, wenn der Anruf beendet ist, wenn es wieder in Excel mithilfe den Funktionszeiger aufruft im _CallBackAddr_ -Argument übergeben. 
    
_ArgCount_
  
> Die Anzahl der an die benutzerdefinierte Funktion zu übergebenden Argumente. Der maximale zulässige Wert beträgt 255.
    
_1. Parameter_
  
> Ein Wert, der benutzerdefinierten Funktion zu übergeben. Wiederholen Sie dieses Argument für jeden Parameter durch _ArgCount_angegeben.
    
## <a name="return-value"></a>R�ckgabewert

**XlHpcRetSuccess** Wenn der UDF-Anruf erfolgreich initiiert wird; **XlHpcRetInvalidSessionId** Wenn das _SessionId_ -Argument ungültig ist; **XlHpcRetCallFailed** bei anderen Fehlern, einschließlich Timeout. Wenn der Anruf alle Fehlercodes (Alles außer **XlHpcRetSuccess**) zurückgibt, klicken Sie dann Excel hält den UDF-Aufruf fehlgeschlagen, macht die _PxAsyncHandle_und davon ausgehen, dass einen Rückruf ausgeführt wurde.
  
## <a name="remarks"></a>Hinweise

Diese Funktion wird asynchron ausgeführt.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

