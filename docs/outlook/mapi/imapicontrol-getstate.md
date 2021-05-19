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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419009"
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
  
> [out] Ein Zeiger auf einen Wert, der den Status des Schaltflächensteuerelements angibt. Einer der folgenden Werte kann zurückgegeben werden:
    
MAPI_DISABLED 
  
> Das Schaltflächensteuerelement ist deaktiviert und kann nicht geklickt werden. 
    
MAPI_ENABLED 
  
> Das Schaltflächensteuerelement ist aktiviert und kann geklickt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status des Schaltflächensteuerelements wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Dienstanbieter implementieren die **IMAPIControl::GetState-Methode,** um MAPI den Status eines Schaltflächensteuerelements zur Verfügung zu stellen. Wenn die Schaltfläche aktiviert ist, kann sie auf einen Mausklick oder eine Tastendrucktaste reagieren. Wenn sie deaktiviert ist, wird die Schaltfläche abgeblendet angezeigt und reagiert nicht auf einen Mausklick oder die Tastendrucktaste. 
  
Weitere Informationen zum Implementieren von **GetState** und den anderen [IMAPIControl : IUnknown-Methoden](imapicontroliunknown.md) finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

