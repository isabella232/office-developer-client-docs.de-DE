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
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280202"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt eine Aufgabe wie das Anzeigen eines Dialogfelds oder das Starten eines programmgesteuerten Vorgangs aus, wenn ein Benutzer der Clientanwendung auf das Schaltflächen-Steuerelement klickt.
  
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
  
> in Ein Handle für das übergeordnete Fenster des Dialogfelds, in dem das Schaltflächen-Steuerelement angezeigt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Schaltflächen-Steuerelement wurde erfolgreich aktiviert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIControl:: Activate** -Methode führt Aufgaben aus, die auf das Klicken des Schaltflächen-Steuerelements durch einen Benutzer folgen. Nachdem der Klick ausgeführt wurde, ruft MAPI im Rahmen der Verarbeitung der Anzeigetabelle einen Aufruf an, um die Aktivierung nach dem ersten Aufruf von [IMAPIControl:: GetState](imapicontrol-getstate.md) zu **aktivieren** , um zu bestimmen, ob die Schaltfläche aktiviert ist. 
  
Weitere Informationen zum Implementieren von **Activate** und den anderen [IMAPIControl: IUnknown](imapicontroliunknown.md) -Methoden finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

