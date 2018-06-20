---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- Debugprintf-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790392"
---
# <a name="debugprintf"></a>debugPrintf

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework Bibliothek-Funktion, die eine Null terminierte Byte-Zeichenfolge in der aktiven Debugger über die Windows SDK-Funktion **OutputDebugStringA**schreibt. Wenn die Anwendung keinen Debugger ist, zeigt der Systemdebugger die Zeichenfolge. Wenn die Anwendung verfügt über keine Debugger und der Systemdebugger nicht aktiv ist, hat **DebugPrintf** keine Auswirkung. 
  
Diese Funktion gibt keinen Wert zurück.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Parameter

 _LpFormat (LPSTR)_
  
Die Formatzeichenfolge, die folgende Syntax und Regeln für, die mit der **Sprintf** -Funktion verwendet. 
  
 _Argumente_
  
NULL oder mehr Argumente, die der Formatzeichenfolge entsprechen.
  
## <a name="example"></a>Beispiel

Diese Funktion gibt eine Zeichenfolge, um anzuzeigen, dass die Steuerung übergeben wurde. _DEBUG-Flag muss vor dem Kompilieren definiert werden, da andernfalls dieser Funktion hat keine Auswirkung.
  
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

