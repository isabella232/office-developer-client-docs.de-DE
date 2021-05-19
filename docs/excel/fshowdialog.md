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
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433591"
---
# <a name="fshowdialog"></a>fShowDialog

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für benutzerdefinierten Befehl, der ein Beispiel für systemeigene Windows lädt und anzeigt. Wenn GENERIC.xll geladen wird, wird ein benutzerdefiniertes Menü, Generic, erstellt, über das auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parameter

Die Funktion nimmt keine Parameter an.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt ganzzahlige Null zurück, um einen erfolgreichen Abschluss anzuzeigen.
  
## <a name="remarks"></a>Hinweise

Die Schritte zum Anzeigen des systemeigenen Windows sind wie folgt:
  
1. Rufen Sie Microsoft Excel Haupthandle Windows **GetHwnd ab.**
    
2. Hook the Excel main window using **HookExcelWindow**.
    
3. Anzeigen des Dialogfelds mithilfe von **DialogBox**.
    
4. Enthook the Excel main window using **UnhookExcelWindow**.
    
### <a name="example"></a>Beispiel

Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

