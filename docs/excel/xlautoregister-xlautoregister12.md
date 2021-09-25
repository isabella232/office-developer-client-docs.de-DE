---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- Xlautoregister-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c43a6248e3d9bb06bcc07c1629846d135b909f5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557582"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel ruft die [xlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) immer dann auf, wenn die XLM-Funktion **REGISTER** oder die C-API-äquivalente [xlfRegister-Funktion](xlfregister-form-1.md)aufgerufen wurde, wobei die Rückgabe- und Argumenttypen der registrierten Funktion fehlen. Damit kann die XLL ihre internen Listen exportierter Funktionen und Befehle durchsuchen, um die Funktion mit dem angegebenen Argument und den angegebenen Rückgabetypen zu registrieren.
  
Ab Excel 2007 ruft Excel die **XlAutoRegister12-Funktion** vor der **XlAutoRegister-Funktion** auf, wenn sie von der XLL exportiert wird. 
  
Excel erfordert keine XLL, um eine dieser Funktionen zu implementieren und zu exportieren.
  
> [!NOTE]
> Wenn **xlAutoRegister** /  **xlAutoRegister12** versucht, die Funktion zu registrieren, ohne das Argument und die Rückgabetypen zu geben, tritt eine rekursive Aufrufschleife auf, die schließlich den Aufrufstapel überschreitet und Excel abstürzt. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parameter

 _pxName_ (**xltypeStr**)
  
Der Name der XLL-Funktion, die registriert wird.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion sollte das Ergebnis des Versuchs zurückgeben, die XLL-Funktion  _pxName_ mithilfe der **xlfRegister-Funktion** zu registrieren. Wenn die angegebene Funktion nicht einer der XLL-Exporte ist, sollte sie die **#VALUE zurückgeben!** oder **NULL,** die Excel bei **#VALUE!** interpretiert.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Implementierung von **xlAutoRegister** sollte eine Suche ohne Groß-/Kleinschreibung durch die internen Listen der Funktionen und Befehle Ihrer XLL durchführen, die exportiert werden, um nach einer Übereinstimmung mit dem übergebenen Namen zu suchen. Wenn die Funktion oder der Befehl gefunden wird, sollte **xlAutoRegister** versuchen, sie mithilfe der **xlfRegister-Funktion** zu registrieren. Stellen Sie dabei sicher, dass Sie die Zeichenfolge angeben, die Excel die Rückgabe- und Argumenttypen der Funktion sowie alle anderen erforderlichen Informationen zur Funktion angibt. Es sollte dann zu Excel zurückkehren, was der Aufruf von **xlfRegister** zurückgegeben hat. Wenn die Funktion erfolgreich registriert wurde, gibt **xlfRegister** einen **xltypeNum-Wert** zurück, der die Register-ID der Funktion enthält. 
  
### <a name="example"></a>Beispiel

Eine Beispielimplementierung dieser Funktion finden Sie in  `SAMPLES\EXAMPLE\EXAMPLE.C` der Datei. 
  
## <a name="see-also"></a>Siehe auch



[REGISTRIEREN](xlfregister-form-1.md)
  
[REGISTRIERUNG](xlfunregister-form-1.md)

