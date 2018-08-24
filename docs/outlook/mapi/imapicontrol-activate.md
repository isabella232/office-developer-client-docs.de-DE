---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580684"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt eine Aufgabe wie etwa Anzeigen eines Dialogfelds oder einen programmgesteuerten Vorgang starten, wenn Benutzer eine Clientanwendung das Button-Steuerelement klickt.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster im Dialogfeld, in dem das Schaltflächensteuerelement angezeigt wird.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Button-Steuerelement wurde erfolgreich aktiviert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIControl::Activate** -Methode führt die Aufgaben, die nach Klicken auf das Schaltflächensteuerelement eines Benutzers. Klicken Sie dann auf als Teil der Verarbeitung der Tabelle anzeigen, tritt nach dem richtet MAPI eines Aufrufs an **Activate** nach der ersten aufrufenden [IMAPIControl::GetState](imapicontrol-getstate.md) um festzustellen, ob die Schaltfläche aktiviert ist. 
  
Weitere Informationen zum **Aktivieren** und die andere implementieren [IMAPIControl: IUnknown](imapicontroliunknown.md) Methoden finden Sie unter [Implementierung der Steuerelement-Objekts](control-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

