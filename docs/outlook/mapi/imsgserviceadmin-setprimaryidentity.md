---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d12795d083053460dc61a2f7e36df3802120665d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579859"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt einen Nachrichtendienst als Lieferanten der primären Identität für das Profil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den Nachrichtendienst zum Bereitstellen der primären Identität enthält, oder NULL, der angibt, dass **SetPrimaryIdentity** die aktuelle Identität löschen soll. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Dem Nachrichtendienst wurde der Lieferant der primären Identität erfolgreich zugewiesen.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** hat versucht, einen Nachrichtendienst festzulegen, für den das SERVICE_NO_PRIMARY_IDENTITY-Flag in der **PR_RESOURCE_FLAGS** -Eigenschaft ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt ist.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::SetPrimaryIdentity-Methode** richtet einen Nachrichtendienst als Lieferanten der primären Identität für das Profil ein. Die primäre Identität ist in der Regel der Benutzer, der beim Nachrichtendienst angemeldet ist. Es wird durch drei Eigenschaften dargestellt: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Jeder Dienstanbieter im angegebenen Nachrichtendienst legt diese drei Eigenschaften auf den Anzeigenamen, den Eintragsbezeichner und den Suchschlüssel des Messagingbenutzers fest, der die primäre Identität bereitstellt. Clients können den Eintragsbezeichner der primären Identität abrufen, indem sie die [IMAPISession::QueryIdentity-Methode](imapisession-queryidentity.md) aufrufen. 
  
Die **PR_RESOURCE_FLAGS-Eigenschaft** ist auf STATUS_PRIMARY_IDENTITY für jeden Anbieter festgelegt, der Mitglied des Nachrichtendiensts ist, der die primäre Identität bereitstellt, und auf SERVICE_PRIMARY_IDENTITY für den Nachrichtendienst. Wenn ein Dienstanbieter die primäre Identität für seinen Nachrichtendienst nicht angeben kann, wird **PR_RESOURCE_FLAGS** auf STATUS_NO_PRIMARY_IDENTITY festgelegt. **SetPrimaryIdentity** legt die **PR_RESOURCE_FLAGS** Eigenschaft jedes Nachrichtendiensts fest, der nicht die primäre Identität auf SERVICE_NO_PRIMARY_IDENTITY angibt. 
  
Jeder Nachrichtendienstanbieter, zu dem die MAPI Informationen enthält, kann eine Identität für jeden benutzer einrichten, wenn sich ein Client beim Dienst anmeldet. Da die MAPI jedoch Verbindungen mit mehreren Dienstanbietern für jede MAPI-Sitzung unterstützt, gibt es keine feste Definition der Identität eines bestimmten Benutzers für die MAPI-Sitzung als Ganzes. Die Identität eines Benutzers hängt davon ab, welcher Dienst beteiligt ist. Clients können **SetPrimaryIdentity** aufrufen, um eine der vielen Identitäten festzulegen, die von Nachrichtendiensten für einen Benutzer als primäre Identität für diesen Benutzer eingerichtet wurden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

