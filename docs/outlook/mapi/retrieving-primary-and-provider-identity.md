---
title: Abrufen der primären und Anbieteridentität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430812"
---
# <a name="retrieving-primary-and-provider-identity"></a>Abrufen der primären und Anbieteridentität

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter, in der Regel Adressbuchanbieter, haben die Möglichkeit, eine Identität zur Darstellung der Sitzung in einer Vielzahl von Situationen zur Verfügung zu stellen. Drei Eigenschaften beschreiben die Identität eines Anbieters:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Diese Eigenschaften werden auf die Eintrags-ID, den Anzeigenamen und den Suchschlüssel des entsprechenden Identitätsobjekts festgelegt, bei dem es sich in der Regel um einen Messagingbenutzer handelt. Anbieter, die eine Identität liefern, legen auch das STATUS_PRIMARY_IDENTITY in ihrer **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) -Eigenschaft fest.
  
Je nach Ihren Anforderungen können Sie die Identität eines bestimmten Anbieters oder die primäre Identität für die Sitzung verwenden. Sie können die Identität eines Anbieters auch zu Anzeigezwecken oder zum Abrufen von Eigenschaften wie PR_RESOURCE_PATH **(** [PidTagResourcePath](pidtagresourcepath-canonical-property.md)) verwenden. **PR_RESOURCE_PATH** enthält , falls festgelegt, den Pfad zu Dateien, die vom Anbieter verwendet oder erstellt wurden. Rufen Sie **die PR_RESOURCE_PATH-Eigenschaft** für den Anbieter ab, der die primäre Identität anliefert, wenn Sie Dateien suchen möchten, die für den Benutzer der Sitzung enthalten sind. 
  
 **So rufen Sie die Identität eines bestimmten Anbieters ab**
  
1. Rufen [Sie IMAPISession::GetStatusTable auf,](imapisession-getstatustable.md) um auf die Statustabelle zu zugreifen. 
    
2. Erstellen Sie eine Einschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um der **spalte PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) mit dem Namen des angegebenen Anbieters zu entsprechen. 
    
3. Rufen [Sie IMAPITable::FindRow auf,](imapitable-findrow.md) um die Zeile des Anbieters zu finden. Die Identität des Anbieters wird in der Spalte **PR_IDENTITY_ENTRYID** gespeichert, falls vorhanden. 
    
 **So rufen Sie die primäre Identität für eine Sitzung ab**
  
- Rufen [Sie IMAPISession::QueryIdentity auf.](imapisession-queryidentity.md) **QueryIdentity** basiert auf dem Vorhandensein des STATUS_PRIMARY_IDENTITY in der spalte **PR_RESOURCE_FLAGS** für eine der Zeilen in der Statustabelle. Wenn keine der Statuszeilen diesen Wert festgelegt hat, weist **QueryIdentity** dem ersten Dienstanbieter, der die drei Eigenschaften PR_IDENTITY, eine Identität zu. Wenn kein Dienstanbieter eine Identität angibt, gibt **QueryIdentity** MAPI_W_NO_SERVICE. In diesem Fall sollten Sie eine Zeichenzeichenfolge erstellen, um einen generischen Benutzer zu repräsentieren, der als primäre Identität dienen kann. 
    
 **So legen Sie die primäre Identität für eine Sitzung explizit**
  
- Rufen [Sie IMsgServiceAdmin::SetPrimaryIdentity auf.](imsgserviceadmin-setprimaryidentity.md) Übergeben Sie **die MAPIUID** für den Zieldienstanbieter. 
    

