---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792074"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Betrifft**: Outlook 
  
Ruft einen Wert, der angibt, ob das Schaltflächensteuerelement aktiviert oder deaktiviert ist.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulState_
  
> [out] Ein Zeiger auf einen Wert, der den Status des Schaltflächen-Steuerelements angibt. Die folgenden Werte kann zurückgegeben werden:
    
MAPI_DISABLED 
  
> Das Button-Steuerelement ist deaktiviert und kann nicht darauf geklickt werden kann. 
    
MAPI_ENABLED 
  
> Das Schaltflächensteuerelement ist aktiviert und geklickt werden kann.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Zustand des Schaltflächensteuerelements wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Dienstanbieter implementieren die **IMAPIControl::GetState** -Methode, um den Status eines Schaltflächen-Steuerelements MAPI bereitzustellen. Wenn die Schaltfläche aktiviert ist, kann es zu einem Klicken mit der Maus oder Drücken einer Taste reagieren. Wenn es deaktiviert ist, wird die Schaltfläche abgeblendet und reagiert nicht auf einer klicken mit der Maus oder Drücken einer Taste. 
  
Weitere Informationen zum Implementieren von **GetState** und ein weiterer [IMAPIControl: IUnknown](imapicontroliunknown.md) Methoden finden Sie unter [Implementierung der Steuerelement-Objekts](control-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

