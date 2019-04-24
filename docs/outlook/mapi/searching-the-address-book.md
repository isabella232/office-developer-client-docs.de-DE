---
title: Durchsuchen des Adressbuchs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d40419291f4b09c5880a769ce231015511e8f269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339739"
---
# <a name="searching-the-address-book"></a>Durchsuchen des Adressbuchs

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI erm�glicht adressbuchanbietern implementierte zwei Stufen von Suchfunktionen zu implementieren:
  
- Eine grundlegende Ebene, die mit einem angegebenen Namen mit der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft von Adressbucheinträgen übereinstimmt. Diese Stufe erm�glicht es Benutzern, beispielsweise Verteilerlisten anzeigen, deren Name mit Nordwest beginnt, oder suchen einzelne messaging Benutzer, deren Nachname Brown ist.
    
- Erweitertes, die auf andere Eigenschaften als **PR_DISPLAY_NAME**entspricht. Diese Stufe erm�glicht es Benutzern, z. B., um ihre Suchanfragen und Benutzer mit dem Namen Brown mit einem bestimmten Adresstyp messaging Find einzugrenzen.
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. Um diese Option auszuwählen, legen Sie das AB_FIND_ON_OPEN-Flag der **PR_CONTAINER_FLAGS** ([pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))-Eigenschaft des Containers fest. After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>Eine einfache Suche in einer Adressbuchcontainer ausf�hren
  
1. Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table. 
    
2. W�hlen Sie eine Suchverfahren, die Ihren Anforderungen entspricht. Die Optionen umfassen:
    
   - [IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table. 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table. 
    
   - [Methode IMAPITable:: Restrict](imapitable-restrict.md) to limit the table view. 
    
   - Eigenschaftseinschränkung mithilfe der **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaft zum Auflösen von mehrdeutigen Namen. Rufen Sie die **Methode IMAPITable:: Restrict**, um diese Einschr�nkung zu erzwingen. 
    
   - [IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names. 
    
3. Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria. **QueryRows** can return zero or more matching rows. 
    
Die Methoden **FindRow**, **SortTable**und **Restrict** werden Tabelle, die f�r jede Tabelle verf�gbar sind, die entweder durch einen Client oder einem Dienstanbieter erstellt werden k�nnen. Die **ANR\_** -Eigenschaftseinschränkung und **IABContainer:: ResolveNames** -Methode von PR sind für Adressbuchanbieter spezifisch und werden zum Auflösen von mehrdeutigen Namen verwendet. Mehrdeutige Namen sind die Eintr�ge in der Empf�ngerliste die keine **PR_ENTRYID** -Eigenschaft zugeordnet sind. 
  
Die **PR\_-ANR** -Einschränkung Ruft einen Algorithmus auf, der eine Zeichenfolge in Wörter trennt und diese Wörter mit Informationen im Adressbuch mithilfe der Präfixübereinstimmung vergleicht. The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).
  
**IABContainer::ResolveNames** f�hrt **PR_ANR** Einschr�nkung Verarbeitung f�r mehrere Namen, ohne den Container Inhaltstabelle ge�ffnet sein. Das einmalige Aufrufen von **ResolveNames** zum Auflösen mehrerer Namen kann viel schneller sein als das mehrfache Aufrufen einer **PR\_-ANR** -Einschränkung. Von adressbuchanbietern implementierte sind jedoch nicht erforderlich, um **ResolveNames**zu unterst�tzen.
  

