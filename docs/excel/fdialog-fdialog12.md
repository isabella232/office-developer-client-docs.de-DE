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
- Fdialog-Funktion [excel 2007], fDialog12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790498"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel benutzerdefinierter Befehl, der veranschaulicht, wie Sie eine Microsoft Excel-UDD (im Dialogfeld benutzerdefinierte) innerhalb einer DLL zu erstellen, indem Sie das Dialogfeld Feld-Funktionen in der C-API. Wenn GENERIC.xll geladen wird, erstellt es ein Menü benutzerdefinierte allgemeine, über die auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Parameter

Die Funktion akzeptiert keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

