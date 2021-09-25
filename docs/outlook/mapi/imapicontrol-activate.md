---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d2a8dcfda03d5bdb058a47fc1b2c0949411fa71a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596351"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt eine Aufgabe aus, z. B. das Anzeigen eines Dialogfelds oder das Starten eines programmgesteuerten Vorgangs, wenn ein Clientanwendungsbenutzer auf das Schaltflächensteuerelement klickt.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des Dialogfelds, in dem das Schaltflächensteuerelement angezeigt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Schaltflächensteuerelement wurde erfolgreich aktiviert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIControl::Activate-Methode** führt Aufgaben nach dem Klicken eines Benutzers auf das Schaltflächensteuerelement aus. Nachdem der Klick erfolgt ist, ruft MAPI im Rahmen der Verarbeitung der Anzeigetabelle **nach** dem ersten Aufrufen von [IMAPIControl::GetState](imapicontrol-getstate.md) die Aktivierung der Schaltfläche auf. 
  
Weitere Informationen zum Implementieren von **Activate** und den anderen [IMAPIControl : IUnknown-Methoden](imapicontroliunknown.md) finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

