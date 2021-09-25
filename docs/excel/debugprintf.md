---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- Debugprintf-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3c09aed1f818c426ed957e3a3273c3bf7f574b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617244"
---
# <a name="debugprintf"></a>debugPrintf

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, die eine Bytezeichenfolge mit Null-Terminierung über die Windows SDK-Funktion **OutputDebugStringA** in den aktiven Debugger schreibt. Wenn die Anwendung keinen Debugger hat, zeigt der Systemdebugger die Zeichenfolge an. Wenn die Anwendung über keinen Debugger verfügt und der Systemdebugger nicht aktiv ist, führt **debugPrintf** keine Aktion aus. 
  
Diese Funktion gibt keinen Wert zurück.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Parameter

 _lpFormat (LPSTR)_
  
Die Formatzeichenfolge, die der Syntax und den Regeln für die Mithilfe der **Sprintf-Funktion** folgt. 
  
 _Argumente_
  
Null oder mehr Argumente, die mit der Formatzeichenfolge übereinstimmen.
  
## <a name="example"></a>Beispiel

Diese Funktion druckt eine Zeichenfolge, um anzuzeigen, dass das Steuerelement an sie übergeben wurde. Das _DEBUG-Flag muss vor der Kompilierung definiert werden, andernfalls führt diese Funktion keine Aktion aus.
  
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

