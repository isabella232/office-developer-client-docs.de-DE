---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fdialog-Funktion [excel 2007],fDialog12-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: afcf924e04f833ff823647eef603824652347e5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568194"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für einen benutzerdefinierten Befehl, der veranschaulicht, wie ein Microsoft Excel UDD (benutzerdefiniertes Dialogfeld) innerhalb einer DLL mithilfe der Dialogfeldfunktionen in der C-API erstellt wird. Beim Laden von GENERIC.xll wird ein benutzerdefiniertes Menü ( Generic) erstellt, über das auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Parameter

Die Funktion akzeptiert keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

