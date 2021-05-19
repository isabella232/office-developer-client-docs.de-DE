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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420094"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Reihenfolge fest, in der Transportanbieter aufgerufen werden, um eine Nachricht zu senden.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parameter

 _cUID_
  
> [in] Die Anzahl eindeutiger Bezeichner im _lpUIDList-Parameter._ 
    
 _lpUIDList_
  
> [in] Ein Zeiger auf ein Array eindeutiger Bezeichner, die Transportanbieter darstellen. Das Array enthält einen Bezeichner für jeden Transportanbieter, der im aktuellen Profil konfiguriert ist.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportauftrag wurde erfolgreich festgelegt.
    
MAPI_E_BUSY 
  
> Der Wert im  _cUID-Parameter_ unterscheidet sich von der Anzahl der Tatsächlichen Transportanbieter im Profil. 
    
MAPI_E_NOT_FOUND 
  
> Mindestens eine der im _lpUIDList-Parameter übergebenen MAPIUID-Strukturen_ bezieht sich nicht auf einen Transportanbieter, der sich derzeit im Profil befindet. [](mapiuid.md) 
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::MsgServiceTransportOrder-Methode** legt die Zustellungsreihenfolge von Transportanbietern in einem Profil fest. Der  _lpUIDList-Parameter_ muss eine sortierte Liste der Transportanbieter-Eintragsbezeichner **enthalten,** die von der PR_PROVIDER_UID ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))-Eigenschaft der Von der [IMsgServiceAdmin::GetProviderTable-Methode zurückgegebenen](imsgserviceadmin-getprovidertable.md) Tabelle erhalten werden. Eine Clientanwendung muss die vollständige Liste in _lpUIDList übergeben._
  
 **SetTransportOrder** überschreibt Transportanbietereinstellungen, z. B. das STATUS_XP_PREFER_LAST, das in der **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

