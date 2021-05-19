---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421165"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel ruft die [xlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) auf, wenn ein Aufruf der XLM-Funktion **REGISTER** oder der C-API-äquivalenten [xlfRegister-Funktion](xlfregister-form-1.md)erfolgt ist, und die Rückgabe- und Argumenttypen der registrierten Funktion fehlen. Die XLL kann ihre internen Listen exportierter Funktionen und Befehle durchsuchen, um die Funktion mit den angegebenen Argument- und Rückgabetypen zu registrieren.
  
Ab Excel 2007 ruft Excel die **xlAutoRegister12-Funktion** vor der **xlAutoRegister-Funktion** auf, wenn sie von der XLL exportiert wird. 
  
Excel erfordert keine XLL zum Implementieren und Exportieren einer dieser Funktionen.
  
> [!NOTE]
> Wenn **xlAutoRegister** /  **xlAutoRegister12** versucht, die Funktion zu registrieren, ohne das Argument und die Rückgabetypen zu liefern, tritt eine rekursive Aufrufschleife auf, die schließlich die Aufrufliste überläuft und Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parameter

 _pxName_ (**xltypeStr**)
  
Der Name der XLL-Funktion, die registriert wird.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion sollte das Ergebnis des Versuches zurückgeben, die XLL-Funktion  _pxName_ mithilfe der **xlfRegister-Funktion zu** registrieren. Wenn die angegebene Funktion nicht zu den Exporten der XLL gehört, sollte die angegebene **#VALUE!** -Fehler oder **NULL,** Excel bei **#VALUE! interpretiert wird.**
  
## <a name="remarks"></a>Hinweise

Ihre Implementierung von **xlAutoRegister** sollte eine Suche ohne Groß-/Kleinschreibung durch die internen Listen ihrer XLL mit den Funktionen und Befehlen durchführen, die exportiert werden, um nach einer Übereinstimmung mit dem übergebenen Namen zu suchen. Wenn die Funktion oder der Befehl gefunden wird, sollte **xlAutoRegister** versuchen, sie mithilfe der **xlfRegister-Funktion** zu registrieren, und stellen Sie sicher, dass die Zeichenfolge, die Excel den Rückgabe- und Argumenttypen der Funktion sowie alle anderen erforderlichen Informationen über die Funktion ans lichte. Sie sollte dann zu Excel zurück, unabhängig davon, welcher Aufruf von **xlfRegister** zurückgegeben wird. Wenn die Funktion erfolgreich registriert wurde, gibt **xlfRegister** einen **xltypeNum-Wert** zurück, der die Register-ID der Funktion enthält. 
  
### <a name="example"></a>Beispiel

Eine  `SAMPLES\EXAMPLE\EXAMPLE.C` Beispielimplementierung dieser Funktion finden Sie in der Datei. 
  
## <a name="see-also"></a>Siehe auch



[REGISTRIEREN](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)

