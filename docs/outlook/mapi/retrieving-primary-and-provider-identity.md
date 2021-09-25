---
title: Abrufen der primären und der Anbieteridentität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6f4aef47d51e129633f51fff6bc7ec874fdc94fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591297"
---
# <a name="retrieving-primary-and-provider-identity"></a>Abrufen der primären und der Anbieteridentität

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter, in der Regel Adressbuchanbieter, haben die Möglichkeit, eine Identität zur Darstellung der Sitzung in einer Vielzahl von Situationen zur Verfügung zu stellen. Drei Eigenschaften beschreiben die Identität eines Anbieters:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Diese Eigenschaften werden auf die Eintrags-ID, den Anzeigenamen und den Suchschlüssel des entsprechenden Identitätsobjekts festgelegt, bei dem es sich in der Regel um einen Messagingbenutzer handelt. Anbieter, die eine Identität angeben, legen auch die STATUS_PRIMARY_IDENTITY-Kennzeichnung in ihrer **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) fest.
  
Je nach Ihren Anforderungen können Sie die Identität eines bestimmten Anbieters oder die primäre Identität für die Sitzung verwenden. Sie können die Identität eines Anbieters auch zum Anzeigen oder Abrufen von Eigenschaften wie **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)) verwenden. **PR_RESOURCE_PATH** enthält, falls festgelegt, den Pfad zu dateien, die vom Anbieter verwendet oder erstellt wurden. Rufen Sie die **PR_RESOURCE_PATH** Eigenschaft für den Anbieter ab, der die primäre Identität angibt, wenn Sie Dateien suchen möchten, die sich auf den Benutzer der Sitzung beziehen. 
  
 **So rufen Sie die Identität eines bestimmten Anbieters ab**
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf die Statustabelle zuzugreifen. 
    
2. Erstellen Sie eine Einschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um die **spalte PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) mit dem Namen des angegebenen Anbieters zuzuordnen. 
    
3. Rufen Sie [IMAPITable::FindRow](imapitable-findrow.md) auf, um die Zeile des Anbieters zu suchen. Die Identität des Anbieters wird in der **spalte PR_IDENTITY_ENTRYID** gespeichert, sofern vorhanden. 
    
 **So rufen Sie die primäre Identität für eine Sitzung ab**
  
- Aufrufen [von IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** basiert die Sitzungsidentität auf dem Vorhandensein des STATUS_PRIMARY_IDENTITY Werts in der **spalte PR_RESOURCE_FLAGS** für eine der Zeilen in der Statustabelle. Wenn keiner der Statuszeilen dieser Wert festgelegt ist, weist **QueryIdentity** dem ersten Dienstanbieter, der die drei PR_IDENTITY Eigenschaften festlegt, eine Identität zu. Wenn kein Dienstanbieter eine Identität bereitstellt, gibt **QueryIdentity** MAPI_W_NO_SERVICE zurück. In diesem Fall sollten Sie eine Zeichenzeichenfolge erstellen, die einen generischen Benutzer darstellt, der als primäre Identität dienen kann. 
    
 **So legen Sie die primäre Identität für eine Sitzung explizit fest**
  
- Rufen [Sie IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)auf. Übergeben Sie die **MAPIUID** für den Zieldienstanbieter. 
    

