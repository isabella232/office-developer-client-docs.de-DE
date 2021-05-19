---
title: Schreiben einer Hierarchieanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421130"
---
# <a name="writing-a-hierarchy-viewer"></a>Schreiben einer Hierarchieanzeige

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Hierarchieanzeiger ist eine Benutzeroberflächenkomponente, die zum Anzeigen von Ordner- und Adressbuchcontainerhierarchietabellen verwendet wird. Hierarchieanzeiger können Elemente der Hierarchie auf unterschiedlichen Ebenen anzeigen und jede Ebene bei Bedarf erweitern und verdingen.
  
Die Containereigenschaft **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) steuert die Ebene, auf der ein Hierarchiemitglied angezeigt wird. Einträge, die Adressbuchcontainer oder Ordner der obersten Ebene darstellen, **PR_DEPTH** auf Null festgelegt. Der Wert dieser Eigenschaft wird sequenziell für Einträge in sequenziellen Ebenen erhöht. Wenn ein Benutzer also einen zu erweiternden Container auf **oberster** Ebene auswählt, werden alle Container mit PR_DEPTH 1 angezeigt. Wenn ein Benutzer einen dieser Untercontainer erweitert,  zeigen Sie die Container mit PR_DEPTH 2 an, und so weiter. 
  
Hierarchieanzeigen unterstützen einen anderen Tiefenbereich. Sie können den Viewer auf nur eine oder zwei Ebenen beschränken oder mehrere Ebenen unterstützen, wenn das Anzeigen einer umfangreichen Hierarchie eine Priorität hat. 
  
Das Adressbuch bietet eine Hierarchieanzeige für die Container auf oberster Ebene im Adressbuch. 
  
 **So greifen Sie auf die Adressbuchhierarchietabelle zu**
  
1. Rufen [Sie IAddrBook::OpenEntry](iaddrbook-openentry.md)auf, und übergeben Sie einen Nulleintragsbezeichner, um den Stammcontainer des Adressbuchs zu öffnen.
    
2. Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des Stammcontainers auf, um auf die Hierarchietabelle des MAPI-Adressbuchs zu zugreifen. 
    
 **So greifen Sie auf die Hierarchietabelle des Standardnachrichtenspeichers zu**
  
1. Rufen [Sie IMAPISession::GetMsgStoresTable auf,](imapisession-getmsgstorestable.md) um auf die Nachrichtenspeichertabelle zu zugreifen. 
    
2. Erstellen Sie eine Einschränkung mithilfe der [SPropertyRestriction-Struktur,](spropertyrestriction.md) um die Tabelle auf die Zeilen zu beschränken, für die **eine PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) -Eigenschaft auf TRUE festgelegt ist. 
    
3. Rufen [Sie IMAPITable::FindRow](imapitable-findrow.md)auf, und übergeben Sie ihn an **die SPropertyRestriction,** um die Zeile zu finden, die den Standardnachrichtenspeicher darstellt. 
    
4. Rufen [Sie IMAPISession::OpenEntry](imapisession-openentry.md)auf, und übergeben Sie die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft aus der Zeile des Standardnachrichtenspeichers in der Nachrichtenspeichertabelle.
    
5. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des **Nachrichtenspeichers** auf, um die PR_IPM_SUBTREE_ENTRYID ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) -Eigenschaft abzurufen.
    
6. Rufen Sie die [IMsgStore::OpenEntry-Methode](imsgstore-openentry.md) des Nachrichtenspeichers auf, und übergeben Sie die **PR_IPM_SUBTREE_ENTRYID-Eigenschaft,** um den Stammordner der IPM-Unterstruktur des Nachrichtenspeichers zu öffnen. 
    
7. Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des IPM-Stammordners auf, um auf die Hierarchietabelle zu zugreifen. 
    

