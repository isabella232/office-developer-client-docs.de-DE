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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5b96a45bab4cd00d23604d0b0b25f3e772277395
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792618"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Betrifft**: Outlook 
  
Legt die Reihenfolge, in welcher, die Transport Anbieter aufgerufen werden, um eine Nachricht zu übermitteln.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parameter

 _cUID_
  
> [in] Die Anzahl der eindeutige Bezeichner in der _LpUIDList_ -Parameter. 
    
 _lpUIDList_
  
> [in] Ein Zeiger auf ein Array Eindeutiger Bezeichner, die Transportanbieter darstellen. Das Array enthält einen Bezeichner für die einzelnen Transportanbieter im aktuellen Profil konfiguriert.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Reihenfolge der Transport wurde erfolgreich festgelegt.
    
MAPI_E_BUSY 
  
> Der Wert in der _cUID_ -Parameter unterscheidet sich von der Anzahl der Transportanbieter tatsächlich im Profil. 
    
MAPI_E_NOT_FOUND 
  
> Eine oder mehrere der in der _LpUIDList_ -Parameter übergeben [MAPIUID](mapiuid.md) Strukturen verweisen nicht auf eine Adressbuchhierarchie derzeit im Profil. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin::MsgServiceTransportOrder** -Methode legt die Reihenfolge der Übermittlung der Transportanbieter in einem Profil. Der _LpUIDList_ -Parameter muss eine sortierte Liste der Adressbuchhierarchie Eintragsbezeichner abgerufen, die aus der Eigenschaft **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) aus der [IMsgServiceAdmin zurückgegebene Tabelle enthalten:: GetProviderTable](imsgserviceadmin-getprovidertable.md) Methode. Eine Clientanwendung muss die vollständige Liste _LpUIDList_übergeben.
  
 **SetTransportOrder** Außerkraftsetzungen transport-Anbieter-Einstellungen wie das STATUS_XP_PREFER_LAST-Flag, das in der Eigenschaft **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

