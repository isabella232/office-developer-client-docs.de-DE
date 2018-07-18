---
title: Verf�gbarmachen von Ordnern in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0e7b479931b6b2b00dd3927133187fe058b4c6e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791642"
---
# <a name="exposing-folders-in-message-stores"></a>Verf�gbarmachen von Ordnern in Nachrichtenspeicher

  
  
**Betrifft**: Outlook 
  
Jede Nachricht Speicheranbieter muss eine der obersten Ebene [IMAPIFolder](imapifolderimapicontainer.md) Benutzeroberfl�che f�r Client-Anwendungen darstellen. Ordner der obersten Ebene entspricht der gesamten Nachrichtenspeicher. Es erm�glicht den Zugriff auf die Ordner, die Benutzern als den Inhalt des Nachrichtenspeichers angezeigt. Dar�ber hinaus Ordner der obersten Ebene wird h�ufig verwendet, wie die Standardeinstellung Empfangsordner f�r IPK Nachrichten und wie der Ordner von denen lesen Berichte gesendet werden. Nachricht-Anbieter m�ssen auch eine IPM-Unterstruktur pr�sentieren � eine Reihe von Ordnern f�r IPM-Nachrichten enthalten � Clientanwendungen. 
  
Client-Anwendungen k�nnen durch Aufrufen der [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode mit 0 und NULL f�r die Parameter  _cbEntryId_ und  _lpEntryId_ jeweils Ordner den obersten Ebene �ffnen. In den meisten F�llen �ffnen Clientanwendungen jedoch den Satz von Ordnern, die IPM Nachrichten enthalten. 
  
Wenn Sie eine Liste der Ordner in den Nachrichtenspeicher IPM Ordnerstruktur erhalten m�chten, verwenden Sie die folgende Schritte aus:
  
1. Verwenden Sie die MAPI-Sitzung, um die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode aufrufen. 
    
2. Verwenden Sie den resultierende Nachricht Datenbankzeiger zum Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode für die **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft.
    
3. Rufen Sie die [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode mit der Eintrags-ID einen **IMAPIFolder** Zeiger abgerufen. 
    
4. Rufen Sie die [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Abrufen einer Tabelle der Inhalt des Ordners. 
    
5. Rufen Sie [die QueryRows, um eine Liste der Ordner im Ordner obersten Ebene](imapitable-queryrows.md) . 
    
MAPI-Clients verwenden diese Ordner Zugriff auf andere Folder-Objekten und Message-Objekte im Nachrichtenspeicher. **IMAPIFolder**und seine �bergeordneten Schnittstelle [IMAPIContainer](imapicontainerimapiprop.md), enthalten die Methoden, die Ihre Nachricht Speicheranbieter implementieren muss, um Ordner mit Message-Objekten Auff�llen und Beantworten von Clientanforderungen auf Nachrichten angewendet werden.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Ordnern in Nachrichtenspeicher](implementing-folders-in-message-stores.md)

