---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- initframework-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420753"
---
# <a name="initframework"></a>InitFramework

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework Library-Funktion, die die Framework-Bibliothek initialisiert, die lediglich die temporären **XLOPER**/ -**XLOPER12** -Speicherdaten Strukturen initialisiert, die bereits zugewiesene Speicher freigeben. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **InitFramework** -Funktion verwendet, um den gesamten temporären Arbeitsspeicher freizugeben. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

