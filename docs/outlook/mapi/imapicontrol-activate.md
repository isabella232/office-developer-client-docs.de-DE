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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418015"
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
  
> [in] Ein Handle zum übergeordneten Fenster des Dialogfelds, in dem das Schaltflächensteuerelement angezeigt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Schaltflächensteuerelement wurde erfolgreich aktiviert.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIControl::Activate-Methode** führt Aufgaben durch, nachdem ein Benutzer auf das Schaltflächensteuerelement geklickt hat. Nachdem der Klick erfolgt ist, ruft MAPI im Rahmen der Verarbeitung der Anzeigetabelle **activate** nach dem ersten Aufruf von [IMAPIControl::GetState](imapicontrol-getstate.md) auf, um zu bestimmen, ob die Schaltfläche aktiviert ist. 
  
Weitere Informationen zum Implementieren von **Activate** und den anderen [IMAPIControl : IUnknown-Methoden](imapicontroliunknown.md) finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

