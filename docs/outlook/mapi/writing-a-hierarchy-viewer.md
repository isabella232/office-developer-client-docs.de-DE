---
title: Schreiben eines Hierarchie-Viewers
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
# <a name="writing-a-hierarchy-viewer"></a>Schreiben eines Hierarchie-Viewers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Hierarchieanzeige ist eine Benutzeroberflächenkomponente, die zum Anzeigen von Ordner-und Adressbuchcontainer-Hierarchietabellen verwendet wird. Hierarchie Betrachter können die Mitglieder der Hierarchie auf verschiedenen Ebenen anzeigen, wobei jede Ebene bei Bedarf erweitert und abgezogen wird.
  
Die Container-Eigenschaft, **PR_DEPTH** ([pidtagdepth (](pidtagdepth-canonical-property.md)), steuert die Ebene, auf der ein Hierarchieelement angezeigt wird. Einträge, die Adressbuchcontainer oder-Ordner der obersten Ebene darstellen, haben Ihre **PR_DEPTH** -Eigenschaft auf NULL festgelegt. Der Wert dieser Eigenschaft wird für Einträge in sequenziellen Ebenen sequenziell erhöht. Wenn ein Benutzer also einen Container der obersten Ebene auswählt, der erweitert werden soll, zeigen Sie alle Container mit **PR_DEPTH** auf 1 festgelegt an. Wenn ein Benutzer einen dieser Untercontainer erweitert, zeigen Sie die Container mit **PR_DEPTH** auf 2 und so weiter an. 
  
Hierarchie Betrachter unterstützen einen unterschiedlichen Tiefen Umfang. Sie können Ihren Viewer auf eine oder zwei Ebenen beschränken, oder Sie können mehrere Ebenen unterstützen, wenn eine expansive Hierarchie eine Priorität darstellt. 
  
Das Adressbuch bietet einen Hierarchie Viewer für die Container der obersten Ebene im Adressbuch. 
  
 **So greifen Sie auf die Adressbuch-Hierarchietabelle zu**
  
1. Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md)auf, und übergeben Sie einen NULL-Eintragsbezeichner, um den Stammcontainer des Adressbuchs zu öffnen.
    
2. Rufen Sie die [IMAPIContainer:: gethierarchyid](imapicontainer-gethierarchytable.md) -Methode des Stammcontainers auf, um auf die Hierarchietabelle des MAPI-Adressbuchs zuzugreifen. 
    
 **So greifen Sie auf die Hierarchietabelle des Standardnachrichten Speichers zu**
  
1. Rufen Sie [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) auf, um auf die Nachrichtenspeichertabelle zuzugreifen. 
    
2. Erstellen Sie eine Einschränkung mithilfe der [SPropertyRestriction](spropertyrestriction.md) -Struktur, um die Tabelle auf die Zeilen einzuschränken, deren **PR_DEFAULT_STORE** ([PIDTAGDEFAULTSTORE (](pidtagdefaultstore-canonical-property.md))-Eigenschaft auf true festgelegt ist. 
    
3. Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md), und übergeben Sie die **SPropertyRestriction**, um die Zeile zu finden, die den Standardnachrichtenspeicher darstellt. 
    
4. Rufen Sie [IMAPISession:: OpenEntry](imapisession-openentry.md)auf, und übergeben Sie die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft aus der Zeile des Standardnachrichten Speichers in der Nachrichtenspeichertabelle.
    
5. Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers auf, um die **PR_IPM_SUBTREE_ENTRYID** ([pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft abzurufen.
    
6. Rufen Sie die [IMsgStore:: OpenEntry](imsgstore-openentry.md) -Methode des Nachrichtenspeichers auf, und übergeben Sie die **PR_IPM_SUBTREE_ENTRYID** -Eigenschaft, um den Stammordner der IPM-Unterstruktur des Nachrichtenspeichers zu öffnen. 
    
7. Rufen Sie die [IMAPIContainer:: gethierarchyid](imapicontainer-gethierarchytable.md) -Methode des IPM-Stammordners auf, um auf die Hierarchietabelle zuzugreifen. 
    

