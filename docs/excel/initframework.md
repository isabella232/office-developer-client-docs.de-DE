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
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790502"
---
# <a name="initframework"></a>InitFramework

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliothek-Funktion, die der Framework-Klassenbibliothek initialisiert die einfach die temporäre **XLOPER**initialisiert/ **XLOPER12** Arbeitsspeicher Datenstrukturen, Freigeben von Speicher, der bereits zugeordnet wurde. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="return-value"></a>R�ckgabewert

Diese Funktion gibt keinen Wert zurück.
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **InitFramework** -Funktion verwendet, alle temporären Speicherplatz freizugeben. 
  
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

