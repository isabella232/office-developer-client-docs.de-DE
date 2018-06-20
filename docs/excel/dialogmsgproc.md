---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- Dialogmsgproc-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790396"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Dieses Verfahren ist zugeordnet, mit dem systemeigenen Windows-Dialogfeld, [fShowDialog](fshowdialog.md) angezeigt. Es bietet die Service-Routinen, die von Windows für die Ereignisse (Nachrichten), die auftreten, wenn der Benutzer des Dialogfelds Schaltflächen, Felder oder Steuerelemente arbeitet aufgerufen. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameter

 _hWndDlg_ (**HWND**)
  
Enthält das HWND Windows Handle des Dialogfelds.
  
 _Nachricht_ (**UINT**)
  
Die Nachricht zu antworten.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Durch Windows übergebene Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

 **True,** Wenn die Nachricht verarbeitet, **FALSE,** Wenn nicht. 
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

