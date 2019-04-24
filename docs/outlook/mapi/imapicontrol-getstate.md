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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280280"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft einen Wert ab, der angibt, ob das Schaltflächen-Steuerelement aktiviert oder deaktiviert ist.
  
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
  
> Out Ein Zeiger auf einen Wert, der den Zustand des Schaltflächen-Steuerelements angibt. Einer der folgenden Werte kann zurückgegeben werden:
    
MAPI_DISABLED 
  
> Das Schaltflächen-Steuerelement ist deaktiviert und kann nicht angeklickt werden. 
    
MAPI_ENABLED 
  
> Das Schaltflächen-Steuerelement ist aktiviert und kann angeklickt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status des Schaltflächen-Steuerelements wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Dienstanbieter implementieren die **IMAPIControl:: GetState** -Methode, um MAPI den Status eines Schaltflächen-Steuerelements bereitzustellen. Wenn die Schaltfläche aktiviert ist, kann Sie auf einen Mausklick oder eine Tastenkombination reagieren. Wenn es deaktiviert ist, wird die Schaltfläche abgeblendet angezeigt und reagiert nicht auf einen Mausklick oder eine Tastenkombination. 
  
Weitere Informationen zum Implementieren von GetState **** und den anderen [IMAPIControl: IUnknown](imapicontroliunknown.md) -Methoden finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

