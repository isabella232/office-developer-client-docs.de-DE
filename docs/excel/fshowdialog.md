---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fshowdialog-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 69c4ba0fc535df6787683a42d49441f97c4bebe4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552248"
---
# <a name="fshowdialog"></a>fShowDialog

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für einen benutzerdefinierten Befehl, der ein systemeigenes Beispiel Windows Dialogfelds lädt und anzeigt. Beim Laden von GENERIC.xll wird ein benutzerdefiniertes Menü ( Generic) erstellt, über das auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parameter

Die Funktion akzeptiert keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt die ganze Zahl Null zurück, um den erfolgreichen Abschluss anzugeben.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Schritte zum Anzeigen des nativen Windows Dialogfelds sind wie folgt:
  
1. Rufen Sie die Microsoft Excel Haupthandle Windows mithilfe von **GetHwnd ab.**
    
2. Hook the Excel main window using **HookExcelWindow**.
    
3. Anzeigen des Dialogfelds mithilfe von **DialogBox**.
    
4. Heben Sie das Excel Hauptfenster mit **unhookExcelWindow auf.**
    
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

