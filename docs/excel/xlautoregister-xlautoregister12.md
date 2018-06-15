---
title: XlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- Xlautoregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19790584"
---
# <a name="xlautoregisterxlautoregister12"></a>XlAutoRegister/xlAutoRegister12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel Ruft die [XlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) , wenn ein Anruf an XLM-Funktion **Registrieren**, oder die C-API entsprechende [XlfRegister-Funktion](xlfregister-form-1.md), mit dem Zurückgeben und -Argument der Funktion registrierende fehlenden vorgenommen wurde. Es ermöglicht die XLL zum Suchen der internen Liste der exportierten Funktionen und Befehle aus, um die Funktion mit dem Argument registrieren und Rückgabetypen angegeben.
  
Ab Excel 2007, ruft Excel die Funktion **xlAutoRegister12** anstelle der **XlAutoRegister** -Funktion aus, wenn es von der XLL exportiert wird. 
  
Excel erforderlich keine XLL zu implementieren und exportieren Sie eine dieser Funktionen.
  
> [!NOTE]
> Wenn **XlAutoRegister**/ **xlAutoRegister12** die Funktion ohne das Argument registrieren und Rückgabetypen versucht, eine rekursive aufrufende Schleife tritt auf, die schließlich überschreitet die Aufrufliste und stürzt Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parameter

 _pxName_ (**XltypeStr**)
  
Der Name der XLL-Funktion, die registriert wird.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Funktion sollte das Ergebnis der Versuch zum Registrieren von XLL-Funktion _PxName_ mithilfe der **XlfRegister** -Funktion zurückgegeben. Wenn die angegebene Funktion nicht von der XLL-Exporten ist, sollte Zurückgeben der **#VALUE!** Fehler oder **NULL** interpretiert Excel am **#VALUE!**.
  
## <a name="remarks"></a>Bemerkungen

Die Implementierung von **XlAutoRegister** sollte eine Groß-/Kleinschreibung unterschieden Suche durchsehen Ihrer XLL interne von Funktionen und Befehle, dass er eine Übereinstimmung mit dem Namen übergebenen Nachrichtensymbol exportiert ausführen. Wenn die Funktion oder den Befehl gefunden werden kann, sollten **XlAutoRegister** versuchen, registrieren, mit der **XlfRegister** -Funktion, wie die Zeichenfolge bereitstellen, auf denen Excel die Return und das Argument Typen von der Funktion als auch andere erforderliche angewiesen wird sichergestellt werden kann Informationen über die Funktion. Dann sollte nach Excel zurückgeben was beim Aufruf von **XlfRegister** zurückgegeben. Wenn die Funktion erfolgreich registriert wurde, gibt **XlfRegister** einen **XltypeNum** -Wert, der mit der ID registrieren der Funktion zurück. 
  
### <a name="example"></a>Beispiel

Finden Sie in der Datei `SAMPLES\EXAMPLE\EXAMPLE.C` für eine Beispiel-Implementierung dieser Funktion. 
  
## <a name="see-also"></a>Siehe auch



[REGISTRIEREN](xlfregister-form-1.md)
  
[AUFHEBEN DER REGISTRIERUNG](xlfunregister-form-1.md)

