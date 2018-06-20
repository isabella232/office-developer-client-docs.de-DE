---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- XlAutoOpen-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790580"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Callback-Funktion, die implementiert und von jedem gültigen XLL exportiert werden muss. Die **XlAutoOpen** -Funktion ist der empfohlene Ausgangspunkt woher Register XLL-Funktionen und Befehle, Initialisieren von Datenstrukturen, Anpassen der Benutzeroberfläche und so weiter. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 (**Int**) zurückgeben.
  
## <a name="remarks"></a>Hinweise

Microsoft Excel **XlAutoOpen** aufgerufen, wenn die XLL aktiviert wird. Die XLL wird in den folgenden Situationen aktiviert: 
  
- Am Anfang einer Excel-Sitzung, wenn es in der letzten Excel-Sitzung aktiv war, die normalerweise beendet.
    
- Wenn während einer Sitzung Excel geladen.
    
- Eine XLL kann auf verschiedene Weise geladen werden:
    
- Wählen Sie **Öffnen** im Menü **Datei** (wobei die Version von Excel diese Methode des Ladens XLLs unterstützt). 
    
- Verwenden Sie den Add-In-Manager.
    
- Aus einer anderen XLL aufruft, [XlfRegister](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument. 
    
- Aus einer XLM-Makrovorlage aufruft, [Registrieren](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument. 
    
- Wenn das Add-in deaktiviert und während einer Sitzung Excel erneut aktiviert ist, wird diese Funktion für eine erneute Aktivierung aufgerufen.
    
### <a name="example"></a>Beispiel

Finden Sie die Dateien `SAMPLES\EXAMPLE\EXAMPLE.C` und `SAMPLES\GENERIC\GENERIC.C`, beispielsweise die Implementierung dieser Funktion und.
  
## <a name="see-also"></a>Siehe auch



[xlAutoClose](xlautoclose.md)
  
[XlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)

