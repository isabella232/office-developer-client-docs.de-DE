---
title: Schreiben eines Hierarchie Viewers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0286696707d268867a5536ef345d0af7909918dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795864"
---
# <a name="writing-a-hierarchy-viewer"></a>Schreiben eines Hierarchie Viewers

  
  
**Betrifft**: Outlook 
  
Ein Hierarchie Viewer ist eine Komponente der Benutzeroberfläche, die für die Anzeige von Ordner Tabellen und Address Book Container Hierarchie verwendet wird. Hierarchie Viewer können Mitglieder der Hierarchie auf verschiedenen Ebenen, erweitern und jede Ebene bei Bedarf vergeben anzuzeigen.
  
Die Container-Eigenschaft **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) steuert die Ebene, auf der Hierarchie Mitglied angezeigt wird. Einträge, die auf oberster Ebene Address Book Container oder Ordner darstellen, haben die **PR_DEPTH** -Eigenschaft auf 0 (null) festgelegt. Der Wert dieser Eigenschaft wird für die Einträge im sequenziellen Ebenen sequenziell erhöht. Legen alle Container mit **PR_DEPTH** auf 1 d. h., wenn der Benutzer einen Container der obersten Ebene wählt zu erweitern, angezeigt. Sobald ein Benutzer eine der folgenden Container erweitert, 2 anzeigen Sie die Container mit **PR_DEPTH** , usw. 
  
Hierarchie Viewer unterstützt einen anderen Bereich mit Tiefen. Sie können Ihre Viewer, nur ein oder zwei Ebenen einschränken oder können Sie mehrere Ebenen unterstützen, wenn der expansiven Hierarchieanzeige eine Priorität ist. 
  
Das Adressbuch bietet einen Hierarchie-Viewer für den Container der obersten Ebene im Adressbuch. 
  
 **Zugriff auf die Address Book Hierarchie-Tabelle**
  
1. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md), übergeben eine null-Eintrags-ID, um Container für das Adressbuch Root zu öffnen.
    
2. Rufen Sie den Container Root [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Zugriff auf die Hierarchietabelle des MAPI-Adressbuchs. 
    
 **Zugriff auf den standardmäßigen Nachrichtenspeicher Hierarchie-Tabelle**
  
1. Rufen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) Zugriff auf die Tabelle Store. 
    
2. Erstellen Sie eine Einschränkung mithilfe der [SPropertyRestriction](spropertyrestriction.md) -Struktur die Tabelle, um nur die Zeilen zu begrenzen, die eine **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))-Eigenschaft auf TRUE festgelegt werden. 
    
3. Rufen Sie [IMAPITable](imapitable-findrow.md), übergeben sie die **SPropertyRestriction**, um zu suchen, die Standard-Informationsspeicher darstellt. 
    
4. Rufen Sie [IMAPISession::OpenEntry](imapisession-openentry.md), aus der Standard-Nachrichtenspeicher Zeile in der Nachricht Store-Tabelle in der Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) übergeben.
    
5. Rufen Sie den Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Rufen Sie den Nachrichtenspeicher [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode übergeben die **PR_IPM_SUBTREE_ENTRYID** -Eigenschaft, um den Stammordner der Nachrichtenspeicher IPM-Unterstruktur zu öffnen. 
    
7. Rufen Sie den Stammordner IPM [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Zugriff auf die Hierarchietabelle. 
    

