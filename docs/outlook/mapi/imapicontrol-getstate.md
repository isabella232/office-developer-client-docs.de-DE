---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a8a24d00aa9646d52f7409c1234eac12109075f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621010"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft einen Wert ab, der angibt, ob das Schaltflächensteuerelement aktiviert oder deaktiviert ist.
  
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
  
> [out] Ein Zeiger auf einen Wert, der den Zustand des Schaltflächensteuerelements angibt. Einer der folgenden Werte kann zurückgegeben werden:
    
MAPI_DISABLED 
  
> Das Schaltflächensteuerelement ist deaktiviert und kann nicht angeklickt werden. 
    
MAPI_ENABLED 
  
> Das Schaltflächensteuerelement ist aktiviert und kann angeklickt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status des Schaltflächensteuerelements wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Dienstanbieter implementieren die **IMAPIControl::GetState-Methode,** um mapi den Status eines Schaltflächensteuerelements bereitzustellen. Wenn die Schaltfläche aktiviert ist, kann sie auf einen Mausklick oder eine Tastenkombination reagieren. Wenn sie deaktiviert ist, wird die Schaltfläche abgeblendet angezeigt und reagiert nicht auf mausklick- oder tastend. 
  
Weitere Informationen zum Implementieren von **GetState** und der anderen [IMAPIControl : IUnknown](imapicontroliunknown.md) -Methoden finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

