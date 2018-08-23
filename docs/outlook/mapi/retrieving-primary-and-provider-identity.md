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
ms.openlocfilehash: da11cf684c4bdcfb94d33791ed7c61d2e322e1a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586585"
---
# <a name="retrieving-primary-and-provider-identity"></a>Abrufen der primären und Anbieteridentität

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter, die in der Regel von adressbuchanbietern implementierte, haben die Möglichkeit eine Identität, die zum Darstellen der Sitzung in einer Vielzahl von Situationen verwendet werden kann. Drei Eigenschaften wird die Identität des Anbieters beschrieben:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Diese Eigenschaften werden festgelegt, um die Eintrags-ID, Anzeigename und Suche-Schlüssel, der die entsprechenden Identitätsobjekt, das in der Regel ein messaging-Benutzer ist. Anbieter, die eine Identität angeben legen Sie das STATUS_PRIMARY_IDENTITY-Flag auch in ihren **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))-Eigenschaft.
  
Je nach Ihren Anforderungen können Sie einen bestimmten Anbieter Identität oder das primäre Identität für die Sitzung verwenden. Sie können die Identität des Anbieters auch für die Anzeige oder zum Abrufen von Eigenschaften, wie beispielsweise **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)) verwenden. **PR_RESOURCE_PATH**, wenn festgelegt ist, enthält den Pfad zu den Dateien vom Anbieter erstellt oder verwendet. Abrufen der **PR_RESOURCE_PATH** -Eigenschaft für den Anbieter für die primäre Identität angeben, wenn Sie Dateien zu suchen, die dem Benutzer der Sitzung gehören möchten. 
  
 **Um die Identität eines bestimmten Anbieters abzurufen.**
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf die Statustabelle. 
    
2. Erstellen Sie eine Einschränkung mithilfe einer [SPropertyRestriction](spropertyrestriction.md) Struktur entsprechend die Spalte **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) mit dem Namen des angegebenen Anbieters. 
    
3. Rufen Sie [IMAPITable](imapitable-findrow.md) , um den Anbieter Zeile zu finden. Identität des Anbieters wird in der Spalte **PR_IDENTITY_ENTRYID** gespeichert werden, sofern vorhanden. 
    
 **Um die primäre Identität für eine Sitzung abzurufen**
  
- Rufen Sie [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** baut Sitzung Identität auf das Vorhandensein der STATUS_PRIMARY_IDENTITY Wert in der Spalte **PR_RESOURCE_FLAGS** für eine der Zeilen in der Tabelle "Status". Wenn keine Zeile Status dieser Wert festgelegt ist, weist **QueryIdentity** Identität zum ersten-Dienstanbieter, der die drei PR_IDENTITY Eigenschaften festlegt. Wenn kein Dienstanbieter eine Identität bereitstellt, gibt **QueryIdentity** MAPI_W_NO_SERVICE zurück. In diesem Fall sollten Sie erstellen eine Zeichenfolge, um einen allgemeinen Benutzer darstellen, der als primäre Identität verwendet werden kann. 
    
 **Die primäre Identität für eine Sitzung explizit festlegen**
  
- Rufen Sie [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Übergeben Sie die **MAPIUID** für den Ziel-Dienstanbieter. 
    

