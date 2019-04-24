---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0a34c441a473154a43a107b4236ccc259d327dba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348055"
---
# <a name="hrcreateofflineobj"></a>HrCreateOfflineObj

**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Erstellt ein MAPI-Offlineobjekt, das vom Anbieter und Speicher verwendet wird, um MAPI zu benachrichtigen, wenn das Objekt Online und offline geschaltet wird. 
  
|||
|:-----|:-----|
|Exportiert von:  <br/> |Msmapi32. dll  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> in Es muss 0 sein.
    
_pCreateInfo_
  
> in Ein Zeiger auf eine **MAPIOFFLINE_CREATEINFO** -Struktur, die die zum Erstellen des Offline Objekts erforderlichen Informationen enthält. 
    
_ppOffline_
  
> Out Ein Zeiger auf die **IMAPIOfflineMgr** -Schnittstelle. 
    
## <a name="return-value"></a>Return value

None.
  
HrOpenOfflineObj
  
## <a name="example"></a>Beispiel

```cpp
// create/get global offline object to use as parent.
 ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = &GUID_GlobalState;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = NULL;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
// Create an offline object for the provider with global as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = pGuid;
  OfflineCreateInfo.pInstance = pInstance;
  OfflineCreateInfo.pParent = pGlobalOfflineMgr;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
  // create store offline object which aggregates with the store object and has provider offline object as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = NULL;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = m_pProviderOfflineMgr;
  OfflineCreateInfo.pMAPISupport = pMAPISup;
  OfflineCreateInfo.pAggregateInfo = &AggregateInfo;
  OfflineCreateInfo.pConnectInfo = NULL;
  ZeroMemory(&AggregateInfo, sizeof(AggregateInfo));
  AggregateInfo.ulSize = sizeof(AggregateInfo);
  AggregateInfo.pOuterObj = (IMsgStore *)this;
  AggregateInfo.pRefTrackRoot = NULL;

```

## <a name="see-also"></a>Siehe auch

- [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)
- [MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

