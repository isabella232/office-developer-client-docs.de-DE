---
title: Schreiben einer Hierarchieanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 462d3ca97dacd231c167fb4834008f4ff79f5c08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619456"
---
# <a name="writing-a-hierarchy-viewer"></a>Schreiben einer Hierarchieanzeige

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Hierarchieanzeige ist eine Benutzeroberflächenkomponente, die zum Anzeigen von Ordner- und Adressbuchcontainerhierarchietabellen verwendet wird. Hierarchiebetrachter können Elemente der Hierarchie auf verschiedenen Ebenen anzeigen und jede Ebene bei Bedarf erweitern und erweitern.
  
Die Containereigenschaft **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) steuert die Ebene, auf der ein Hierarchieelement angezeigt wird. Bei Einträgen, die Adressbuchcontainer oder Ordner auf oberster Ebene darstellen, ist die **PR_DEPTH** Eigenschaft auf Null festgelegt. Der Wert dieser Eigenschaft wird für Einträge in sequenziellen Ebenen sequenziell erhöht. Wenn ein Benutzer also einen Container auf oberster Ebene auswählt, der erweitert werden soll, werden alle Container mit **PR_DEPTH** auf 1 festgelegt. Wenn ein Benutzer einen dieser Untercontainer erweitert, zeigen Sie die Container mit **PR_DEPTH** auf 2 festgelegt usw. an. 
  
Hierarchieanzeigen unterstützen einen anderen Tiefenbereich. Sie können Den Betrachter auf eine oder zwei Ebenen beschränken oder mehrere Ebenen unterstützen, wenn das Anzeigen einer hierarchischen Hierarchie Priorität hat. 
  
Das Adressbuch stellt eine Hierarchieanzeige für die Container auf oberster Ebene im Adressbuch bereit. 
  
 **So greifen Sie auf die Adressbuchhierarchietabelle zu**
  
1. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md)auf, indem Sie einen NULL-Eintragsbezeichner übergeben, um den Stammcontainer des Adressbuchs zu öffnen.
    
2. Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des Stammcontainers auf, um auf die Hierarchietabelle des MAPI-Adressbuchs zuzugreifen. 
    
 **So greifen Sie auf die Hierarchietabelle des Standardnachrichtenspeichers zu**
  
1. Rufen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) auf, um auf die Nachrichtenspeichertabelle zuzugreifen. 
    
2. Erstellen Sie eine Einschränkung mithilfe der [SPropertyRestriction-Struktur,](spropertyrestriction.md) um die Tabelle auf die Zeilen zu beschränken, für die eine **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) -Eigenschaft auf TRUE festgelegt ist. 
    
3. Rufen Sie [IMAPITable::FindRow](imapitable-findrow.md)auf, übergeben Sie es an **SPropertyRestriction,** um die Zeile zu suchen, die den Standardnachrichtenspeicher darstellt. 
    
4. Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.
    
5. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers auf, um die **eigenschaft PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) abzurufen.
    
6. Rufen Sie die [IMsgStore::OpenEntry-Methode](imsgstore-openentry.md) des Nachrichtenspeichers auf, und übergeben Sie die **PR_IPM_SUBTREE_ENTRYID-Eigenschaft,** um den Stammordner der IPM-Unterstruktur des Nachrichtenspeichers zu öffnen. 
    
7. Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des IPM-Stammordners auf, um auf die Hierarchietabelle zuzugreifen. 
    

