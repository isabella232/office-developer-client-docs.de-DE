---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303948"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel Ruft die [xlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) immer dann auf, wenn ein Aufruf an das XML-Funktions **Register**oder die äquivalente [XLFREGISTER-Funktion](xlfregister-form-1.md)der C-API erfolgt, wobei die Rückgabe-und Argumenttypen der registrierten Funktion fehlen. Es ermöglicht der XLL, die internen Listen der exportierten Funktionen und Befehle zu durchsuchen, um die Funktion mit dem angegebenen Argument und den zurückgegebenen Rückgabetypen zu registrieren.
  
Ab Excel 2007 ruft Excel die **xlAutoRegister12** -Funktion bevorzugt für die **xlAutoRegister** -Funktion auf, wenn Sie von der XLL exportiert wird. 
  
Excel erfordert keine XLL zum Implementieren und Exportieren einer dieser Funktionen.
  
> [!NOTE]
> Wenn **xlAutoRegister**/ **xlAutoRegister12** versucht, die Funktion ohne Angabe des Arguments und der Rückgabetypen zu registrieren, tritt eine rekursive Aufruf Schleife auf, die schließlich die Aufrufliste überschreitet und Excel abstürzt. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parameter

 _pxName_ (**xltypeStr**)
  
Der Name der XLL-Funktion, die registriert wird.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion sollte das Ergebnis des Versuchs zurückgeben, die XLL-Funktion _pxName_ mithilfe der **xlfRegister** -Funktion zu registrieren. Wenn es sich bei der angegebenen Funktion nicht um einen Export der XLL handelt, sollte Sie die #VALUE zurückgeben **!** Fehler oder **null** , die Excel bei **#VALUE!** interpretiert.
  
## <a name="remarks"></a>Bemerkungen

Bei der Implementierung von **xlAutoRegister** sollte bei der Suche nach einer Übereinstimmung mit dem übergebenen Namen durch die internen Listen der Funktionen und Befehle, die exportiert werden soll, eine Groß-/Kleinschreibung nicht beachtet werden. Wenn die Funktion oder der Befehl gefunden wird, sollte **xlAutoRegister** versuchen, Sie zu registrieren, indem Sie die **xlfRegister** -Funktion verwenden, indem Sie sicherstellen, dass die Zeichenfolge bereitGestellt wird, die Excel die Rückgabe-und Argumenttypen der Funktion sowie alle anderen erforderlichen Informationen zur Funktion. Sie sollte dann zu Excel zurückkehren, unabhängig vom Aufruf von **xlfRegister** zurückgegeben. Wenn die Funktion erfolgreich registriert wurde, gibt **xlfRegister** einen **xltypeNum** -Wert zurück, der die Register-ID der Funktion enthält. 
  
### <a name="example"></a>Beispiel

Eine Beispielimplementierung `SAMPLES\EXAMPLE\EXAMPLE.C` dieser Funktion finden Sie in der Datei. 
  
## <a name="see-also"></a>Siehe auch



[Registrieren](xlfregister-form-1.md)
  
[Registrierung](xlfunregister-form-1.md)

