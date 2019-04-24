---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310003"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Reihenfolge fest, in der Transportanbieter aufgerufen werden, um eine Nachricht zu übermitteln.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parameter

 _cUID_
  
> in Die Anzahl der eindeutigen Bezeichner im _lpUIDList_ -Parameter. 
    
 _lpUIDList_
  
> in Ein Zeiger auf ein Array von eindeutigen Bezeichnern, die Transportanbieter darstellen. Das Array enthält einen Bezeichner für jeden Transportanbieter, der im aktuellen Profil konfiguriert ist.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportauftrag wurde erfolgreich festgelegt.
    
MAPI_E_BUSY 
  
> Der Wert im Parameter _cUID_ unterscheidet sich von der Anzahl der Transportanbieter tatsächlich im Profil. 
    
MAPI_E_NOT_FOUND 
  
> Mindestens eine der [MAPIUID](mapiuid.md) -Strukturen, die im _lpUIDList_ -Parameter übergeben werden, beziehen sich nicht auf einen Transportanbieter, der sich derzeit im Profil befindet. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin:: MsgServiceTransportOrder** -Methode legt die Übermittlungsreihenfolge der Transportanbieter in einem Profil fest. Der _lpUIDList_ -Parameter muss eine sortierte Liste der Transportanbieter-Eintrags-IDs enthalten, die von der **PR_PROVIDER_UID** ([pidtagprovideruid (](pidtagprovideruid-canonical-property.md))-Eigenschaft der Tabelle abgerufen werden, die von der IMsgServiceAdmin zurückgegeben wird [: ](imsgserviceadmin-getprovidertable.md)Getproviderable-Methode. Eine Clientanwendung muss die vollständige Liste in _lpUIDList_.
  
 **SetTransportOrder** überschreibt Transportanbieter Einstellungen wie das STATUS_XP_PREFER_LAST-Flag, das in der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

