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
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430364"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt einen Nachrichtendienst als Anbieter der primären Identität für das Profil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den Nachrichtendienst enthält, um die primäre Identität anzugeben, oder NULL, der angibt, dass **SetPrimaryIdentity** die aktuelle Identität löschen soll. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Dem Nachrichtendienst wurde der Anbieter der primären Identität erfolgreich zugewiesen.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** hat versucht, einen Nachrichtendienst zu bestimmen, für den das SERVICE_NO_PRIMARY_IDENTITY-Flag in seiner **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt ist.
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::SetPrimaryIdentity-Methode** richtet einen Nachrichtendienst als Anbieter der primären Identität für das Profil ein. Die primäre Identität ist in der Regel der Benutzer, der beim Nachrichtendienst angemeldet ist. Es wird durch drei Eigenschaften dargestellt: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Jeder Dienstanbieter im angegebenen Nachrichtendienst legt diese drei Eigenschaften auf den Anzeigenamen, die Eintrags-ID und den Suchschlüssel des Messagingbenutzers fest, der die primäre Identität liefert. Clients können den Eintragsbezeichner der primären Identität abrufen, indem sie die [IMAPISession::QueryIdentity-Methode](imapisession-queryidentity.md) aufrufen. 
  
Die **PR_RESOURCE_FLAGS-Eigenschaft** ist auf STATUS_PRIMARY_IDENTITY für jeden Anbieter festgelegt, der Mitglied des Nachrichtendiensts ist, der die primäre Identität liefert, und auf SERVICE_PRIMARY_IDENTITY für den Nachrichtendienst festgelegt. Wenn ein Dienstanbieter die primäre Identität für seinen Nachrichtendienst nicht liefern kann, wird **PR_RESOURCE_FLAGS** auf STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** legt **die PR_RESOURCE_FLAGS** der einzelnen Nachrichtendienste fest, die die primäre Identität nicht für SERVICE_NO_PRIMARY_IDENTITY. 
  
Jeder Nachrichtendienstanbieter, zu dem MAPI Informationen hat, kann eine Identität für jeden seiner Benutzer einrichten, wenn sich ein Client beim Dienst anmeldet. Da MAPI jedoch Verbindungen zu mehreren Dienstanbietern für jede #A0 unterstützt, gibt es keine feste Definition der Identität eines bestimmten Benutzers für die #A1 insgesamt. Die Identität eines Benutzers hängt davon ab, welcher Dienst beteiligt ist. Clients können **SetPrimaryIdentity aufrufen,** um eine der vielen Identitäten zu bestimmen, die von Nachrichtendiensten für einen Benutzer als primäre Identität für den Benutzer eingerichtet wurden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

