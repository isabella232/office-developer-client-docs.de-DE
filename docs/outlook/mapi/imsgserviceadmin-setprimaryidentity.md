---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 92807cb216e8a7f4eef6b4d95a8d12826b176e6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564668"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Legt eine Message Service hat der Hersteller der primäre Identität für das Profil sein.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Dienst angeben die primäre Identität enthält, oder NULL, gibt an, dass die aktuelle Identität **SetPrimaryIdentity** gelöscht werden sollte. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich hat den Hersteller der primären Identität zugewiesen.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** wurde versucht, eine Message Service angeben, die das SERVICE_NO_PRIMARY_IDENTITY-Flag, das in der **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt wurde.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Methode **IMsgServiceAdmin::SetPrimaryIdentity** richtet einen Nachrichtendienst zur als hat der Hersteller der primäre Identität für das Profil. Die primäre Identität ist in der Regel der Benutzer, die den Dienst angemeldet ist. Es wird durch drei Eigenschaften dargestellt: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Jeder Dienstanbieter in der festgelegten Messagingdiensts wird diese drei Eigenschaften auf die Anzeigenamen sowie die Eintrags-ID und Suche Schlüssel des Benutzers messaging, das die primäre Identität bereitstellt. Clients können die primäre Identität Eintrags-ID abrufen, durch die [IMAPISession::QueryIdentity](imapisession-queryidentity.md) -Methode aufrufen. 
  
Die **PR_RESOURCE_FLAGS** -Eigenschaft wird festgelegt, um STATUS_PRIMARY_IDENTITY für die einzelnen Anbieter, die den Dienst gehört, das die primäre Identität bereitstellt und SERVICE_PRIMARY_IDENTITY für den Dienst. Bei ein Dienstanbieter die primäre Identität für die Message-Dienst angegeben werden kann, wird es auf STATUS_NO_PRIMARY_IDENTITY **PR_RESOURCE_FLAGS** . **SetPrimaryIdentity** wird die **PR_RESOURCE_FLAGS** -Eigenschaft der einzelnen Nachricht-Dienste, die nicht der primäre Identitätswert SERVICE_NO_PRIMARY_IDENTITY bereitstellt. 
  
Jeder Nachricht-Dienstanbieter, die MAPI Informationen zu verfügt kann beim Anmelden eines Clients mit dem Dienst auf eine Identität für jeden Benutzer einrichten. Da MAPI-Verbindungen mit mehreren Dienstanbieter für jede MAPI-Sitzung unterstützt, ist es jedoch keine feste Definition der Identität eines bestimmten Benutzers für die MAPI-Sitzung als Ganzes. Identität des Benutzers, hängt davon ab, welcher Dienst beteiligt ist. Clients können **SetPrimaryIdentity** zum Bestimmen von einer der vielen Identitäten eingerichtet für einen Benutzer von den Diensten für die Nachricht als primäre Identität für diesen Benutzer aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

