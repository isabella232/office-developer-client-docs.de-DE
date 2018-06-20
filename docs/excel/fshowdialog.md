---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fShowDialog-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790512"
---
# <a name="fshowdialog"></a>fShowDialog

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel benutzerdefinierter Befehl, der geladen und ein Beispiel systemeigenen Windows-Dialogfeld angezeigt. Wenn GENERIC.xll geladen wird, erstellt es ein Menü benutzerdefinierte allgemeine, über die auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parameter

Die Funktion akzeptiert keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Funktion return ganze Zahl 0 (null) an, dass erfolgreiche Abschluss
  
## <a name="remarks"></a>Hinweise

Die Schritte zum Anzeigen des systemeigenen Windows-Dialogfeld sind wie folgt:
  
1. Abrufen von **GetHwnd**Hauptfenster Microsoft Excel-Windows-Handles.
    
2. Das Excel-Hauptfenster mit **HookExcelWindow**zu verknüpfen.
    
3. Zeigt das Dialogfeld **DialogBox**verwenden.
    
4. Aufzuheben Sie das Excel-Hauptfenster mit **UnhookExcelWindow**.
    
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

