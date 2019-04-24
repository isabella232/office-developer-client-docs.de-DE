---
title: Abrufen der primären und Anbieter Identität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328637"
---
# <a name="retrieving-primary-and-provider-identity"></a>Abrufen der primären und Anbieter Identität

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter, in der Regel Adressbuchanbieter, haben die Möglichkeit, eine Identität anzugeben, die verwendet werden kann, um die Sitzung in einer Vielzahl von Situationen darzustellen. Drei Eigenschaften beschreiben die Identität eines Anbieters:
  
- **PR_IDENTITY_ENTRYID** ([Pidtagidentityentryid (](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([Pidtagidentitydisplay (](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([Pidtagidentitysearchkey (](pidtagidentitysearchkey-canonical-property.md)) 
    
Diese Eigenschaften werden auf die Eintrags-ID, den Anzeigenamen und den Suchschlüssel des entsprechenden Identity-Objekts festgelegt, bei dem es sich in der Regel um einen Messagingbenutzer handelt. Anbieter, die eine Identität angeben, legen auch das STATUS_PRIMARY_IDENTITY-Flag in Ihrer **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft fest.
  
Je nach Ihren Anforderungen können Sie die Identität eines bestimmten Anbieters oder die primäre Identität für die Sitzung verwenden. Sie können die Identität eines Anbieters auch zu Anzeigezwecken oder zum Abrufen von Eigenschaften wie **PR_RESOURCE_PATH** ([pidtagresourcepath (](pidtagresourcepath-canonical-property.md)) verwenden. **PR_RESOURCE_PATH**, wenn festgelegt, enthält den Pfad zu Dateien, die vom Anbieter verwendet oder erstellt werden. Rufen Sie die **PR_RESOURCE_PATH** -Eigenschaft für den Anbieter ab, der die primäre Identität angibt, wenn Sie Dateien suchen möchten, die für den Benutzer der Sitzung relevant sind. 
  
 **So rufen Sie die Identität eines bestimmten Anbieters ab**
  
1. Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf die Statustabelle zuzugreifen. 
    
2. Erstellen Sie eine Einschränkung mithilfe einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, um die **PR_PROVIDER_DLL_NAME** ([pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md))-Spalte mit dem Namen des angegebenen Anbieters zu vergleichen. 
    
3. Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md) auf, um die Zeile des Anbieters zu finden. Die Identität des Anbieters wird in der **PR_IDENTITY_ENTRYID** -Spalte gespeichert, sofern vorhanden. 
    
 **So rufen Sie die primäre Identität für eine Sitzung ab**
  
- Rufen Sie [IMAPISession:: QueryIdentity](imapisession-queryidentity.md)auf. **QueryIdentity** basiert die Sitzungs Identität auf dem vorhanden sein des STATUS_PRIMARY_IDENTITY-Werts in der **PR_RESOURCE_FLAGS** -Spalte für eine der Zeilen in der Status Tabelle. Wenn für keine der Statuszeilen dieser Wert festgelegt ist, weist **QueryIdentity** dem ersten Dienstanbieter die Identität zu, der die drei PR_IDENTITY-Eigenschaften festlegt. Wenn kein Dienstanbieter eine Identität bereitstellt, gibt **QUERYIDENTITY** MAPI_W_NO_SERVICE zurück. In diesem Fall sollten Sie eine Zeichenfolge erstellen, die einen generischen Benutzer darstellt, der als primäre Identität dienen kann. 
    
 **So legen Sie die primäre Identität für eine Sitzung explizit fest**
  
- Rufen Sie [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)auf. Führen Sie die **MAPIUID** für den Zieldienst Anbieter aus. 
    

