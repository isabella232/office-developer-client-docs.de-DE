---
title: Suchen im Adressbuch
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0d3fb5d2ce5036c6491e24bba8d3541b123eaab1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595125"
---
# <a name="searching-the-address-book"></a>Suchen im Adressbuch

**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI erm�glicht adressbuchanbietern implementierte zwei Stufen von Suchfunktionen zu implementieren:
  
- Eine grundlegende Ebene, die mit einen angegebenen Namen mit der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft von Adressbucheinträgen übereinstimmt. Diese Stufe erm�glicht es Benutzern, beispielsweise Verteilerlisten anzeigen, deren Name mit Nordwest beginnt, oder suchen einzelne messaging Benutzer, deren Nachname Brown ist.
    
- Erweitertes, die auf andere Eigenschaften als **PR_DISPLAY_NAME**entspricht. Diese Stufe erm�glicht es Benutzern, z. B., um ihre Suchanfragen und Benutzer mit dem Namen Brown mit einem bestimmten Adresstyp messaging Find einzugrenzen.
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. Wenn Sie diese Option auswählen, festlegen Sie AB_FIND_ON_OPEN das Flag des Containers **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))-Eigenschaft. After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>Eine einfache Suche in einer Adressbuchcontainer ausf�hren
  
1. Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table. 
    
2. W�hlen Sie eine Suchverfahren, die Ihren Anforderungen entspricht. Die Optionen umfassen:
    
   - [IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table. 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table. 
    
   - [Methode IMAPITable:: Restrict](imapitable-restrict.md) to limit the table view. 
    
   - Eigenschaftseinschränkung über die **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md))-Eigenschaft für das Auflösen von Namen nicht eindeutig. Rufen Sie die **Methode IMAPITable:: Restrict**, um diese Einschr�nkung zu erzwingen. 
    
   - [IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names. 
    
3. Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria. **QueryRows** can return zero or more matching rows. 
    
Die Methoden **FindRow**, **SortTable**und **Restrict** werden Tabelle, die f�r jede Tabelle verf�gbar sind, die entweder durch einen Client oder einem Dienstanbieter erstellt werden k�nnen. Die **PR\_ANR** eigenschaftseinschränkung und **IABContainer** -Methode für adressbuchanbietern implementierte spezifisch sind, und zum Auflösen von Namen mehrdeutige verwendet werden. Mehrdeutige Namen sind die Eintr�ge in der Empf�ngerliste die keine **PR_ENTRYID** -Eigenschaft zugeordnet sind. 
  
Die **PR\_ANR** Einschränkung Ruft einen Algorithmus, der trennt einer Zeichenfolge in Wörter und diese Wörter mit Informationen im Adressbuch mit präfixvergleich übereinstimmt. The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).
  
**IABContainer::ResolveNames** f�hrt **PR_ANR** Einschr�nkung Verarbeitung f�r mehrere Namen, ohne den Container Inhaltstabelle ge�ffnet sein. **ResolveNames** einmal aufrufen, um mehrere Namen auflösen kann sehr viel schneller Aufrufen einer **PR\_ANR** Einschränkung mehrmals. Von adressbuchanbietern implementierte sind jedoch nicht erforderlich, um **ResolveNames**zu unterst�tzen.
  

