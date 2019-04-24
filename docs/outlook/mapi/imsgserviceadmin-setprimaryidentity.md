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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317360"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt fest, dass ein Nachrichtendienst der Lieferant der primären Identität für das Profil ist.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Nachrichtendienst enthält, um die primäre Identität anzugeben, oder NULL, die angibt, dass **SetPrimaryIdentity** die aktuelle Identität löschen soll. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Dem Nachrichtendienst wurde der Lieferant mit der primären Identität erfolgreich zugewiesen.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** hat versucht, einen Nachrichtendienst mit dem SERVICE_NO_PRIMARY_IDENTITY-Flag in seiner **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft festzulegen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin:: SetPrimaryIdentity** -Methode richtet einen Nachrichtendienst als Anbieter der primären Identität für das Profil ein. Die primäre Identität ist in der Regel der Benutzer, der beim Nachrichtendienst angemeldet ist. Es wird durch drei Eigenschaften dargestellt: 
  
- **PR_IDENTITY_DISPLAY** ([Pidtagidentitydisplay (](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([Pidtagidentityentryid (](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([Pidtagidentitysearchkey (](pidtagidentitysearchkey-canonical-property.md))
    
Jeder Dienstanbieter im angegebenen Nachrichtendienst legt diese drei Eigenschaften auf den Anzeigenamen, die Eintrags-ID und den Suchschlüssel des Messaging Benutzers fest, der die primäre Identität bereitstellt. Clients können die Eintrags-ID der primären Identität abrufen, indem Sie die [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) -Methode aufrufen. 
  
Die **PR_RESOURCE_FLAGS** -Eigenschaft wird für jeden Anbieter, der ein Mitglied des Nachrichtendiensts ist, der die primäre Identität bereitstellt, und SERVICE_PRIMARY_IDENTITY für den Nachrichtendienst auf STATUS_PRIMARY_IDENTITY festgelegt. Wenn ein Dienstanbieter die primäre Identität für seinen Nachrichtendienst nicht angeben kann, wird **PR_RESOURCE_FLAGS** auf STATUS_NO_PRIMARY_IDENTITY festgelegt. **SetPrimaryIdentity** legt die **PR_RESOURCE_FLAGS** -Eigenschaft der einzelnen Nachrichtendienste fest, die nicht die primäre Identität für SERVICE_NO_PRIMARY_IDENTITY bereitstellen. 
  
Jeder Nachrichtendienst Anbieter, über den MAPI Informationen enthält, kann für jeden seiner Benutzer eine Identität festlegen, wenn sich ein Client beim Dienst anmeldet. Da MAPI jedoch Verbindungen mit mehreren Dienstanbietern für jede MAPI-Sitzung unterstützt, gibt es keine feste Definition der Identität eines bestimmten Benutzers für die MAPI-Sitzung als Ganzes; die Identität eines Benutzers hängt davon ab, welcher Dienst beteiligt ist. Clients können **SetPrimaryIdentity** aufrufen, um eine der vielen Identitäten festzulegen, die von Nachrichtendiensten für einen Benutzer als primäre Identität für diesen Benutzer erstellt wurden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

