---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- dialogmsgpaw-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f93be01679460833d9555cc747ff72d9b1d5b6fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625966"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Diese Prozedur ist dem systemeigenen Windows Dialogfeld zugeordnet, das [von fShowDialog](fshowdialog.md) angezeigt wird. Es stellt die Dienstroutinen bereit, die von Windows für die Ereignisse (Nachrichten) aufgerufen werden, die auftreten, wenn der Benutzer eine der Schaltflächen, Eingabefelder oder Steuerelemente des Dialogfelds ausführt. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameter

 _hWndDlg_ (**HWND**)
  
Enthält das HWND-Windows Handle des Dialogfelds.
  
 _message_ (**UINT**)
  
Die Nachricht, auf die reagiert werden soll.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Von Windows übergebene Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 **TRUE,** wenn nachricht verarbeitet, **FALSE,** wenn nicht. 
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

