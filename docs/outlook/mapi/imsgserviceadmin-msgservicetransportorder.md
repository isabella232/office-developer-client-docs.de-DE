---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cc9efe43bcccf0af6f0b67e2091e4490234bbc3b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610419"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Reihenfolge fest, in der Transportanbieter aufgerufen werden, um eine Nachricht zuzustellen.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parameter

 _Cuid_
  
> [in] Die Anzahl der eindeutigen Bezeichner im _lpUIDList-Parameter._ 
    
 _lpUIDList_
  
> [in] Ein Zeiger auf ein Array eindeutiger Bezeichner, die Transportanbieter darstellen. Das Array enthält einen Bezeichner für jeden Transportanbieter, der im aktuellen Profil konfiguriert ist.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportauftrag wurde erfolgreich festgelegt.
    
MAPI_E_BUSY 
  
> Der Wert im  _cUID-Parameter_ unterscheidet sich von der Anzahl der Transportanbieter im Profil. 
    
MAPI_E_NOT_FOUND 
  
> Eine oder mehrere der [mapiuid-Strukturen,](mapiuid.md) die im  _lpUIDList-Parameter_ übergeben werden, beziehen sich nicht auf einen Transportanbieter, der sich derzeit im Profil enthält. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::MsgServiceTransportOrder-Methode** legt den Lieferauftrag von Transportanbietern in einem Profil fest. Der  _parameter lpUIDList_ muss eine sortierte Liste von Transportanbieter-Eintragsbezeichnern enthalten, die von der **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) -Eigenschaft der Tabelle abgerufen werden, die von der [IMsgServiceAdmin::GetProviderTable-Methode](imsgserviceadmin-getprovidertable.md) zurückgegeben wird. Eine Clientanwendung muss die vollständige Liste in  _lpUIDList_ übergeben.
  
 **SetTransportOrder** setzt Transportanbietereinstellungen außer Kraft, z. B. das STATUS_XP_PREFER_LAST Flag, das in der **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

