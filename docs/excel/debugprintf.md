---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424798"
---
# <a name="debugprintf"></a>debugPrintf

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, die eine mit NULL endende Byte-Zeichenfolge in den aktiven Debugger über die Windows SDK-Funktion **OutputDebugStringA**schreibt. Wenn die Anwendung keinen Debugger hat, zeigt der Systemdebugger die Zeichenfolge an. Wenn die Anwendung keinen Debugger hat und der Systemdebugger nicht aktiv ist, wird von **debugPrintf** keine Aktion ausgeführt. 
  
Diese Funktion gibt keinen Wert zurück.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Parameter

 _lpFormat (LPSTR)_
  
Die Formatzeichenfolge, die die Syntax und Regeln für die mit der **sprintf** -Funktion verwendete folgt. 
  
 _Argumente_
  
NULL oder mehr Argumente, die mit der Formatzeichenfolge übereinstimmen.
  
## <a name="example"></a>Beispiel

Diese Funktion druckt eine Zeichenfolge, um anzuzeigen, dass das Steuerelement an Sie übergeben wurde. Das _DEBUG-Flag muss vor dem Kompilieren definiert werden, sonst hat diese Funktion nichts.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

