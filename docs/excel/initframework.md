---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- Initframework-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 932d1a42c104b364d6f6d584e4e8848469405688
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621430"
---
# <a name="initframework"></a>InitFramework

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktion, die die Framework-Bibliothek initialisiert, die einfach die **temporären XLOPER** /  **XLOPER12-Speicherdatenstrukturen** initialisiert und bereits zugewiesenen Speicher freigibt. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **InitFramework-Funktion** verwendet, um den gesamten temporären Speicher freizugeben. 
  
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

