---
title: Verf�gbarmachen von Ordnern in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 457620dd0f805e78d12fc8feba09f8fc8aedc554
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341349"
---
# <a name="exposing-folders-in-message-stores"></a>Verfügbarmachen von Ordnern in Nachrichtenspeichern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jeder Nachrichtenspeicheranbieter muss für Clientanwendungen eine [IMAPIFolder](imapifolderimapicontainer.md)-Schnittstelle auf oberster Ebene präsentieren. Der Ordner auf oberster Ebene entspricht dem gesamten Nachrichtenspeicher; er bietet Zugriff auf die Ordner, die Benutzer als die Inhalte des Nachrichtenspeichers sehen. Außerdem wird der Ordner auf oberster Ebene häufig als Standardempfangsordner für IPC-Nachrichten und als der Ordner verwendet, von dem aus Leseberichte gesendet werden. Nachrichtenspeicheranbieter müssen für Clientanwendungen auch eine IPM-Unterstruktur präsentieren, eine Reihe von Ordnern, in denen IPM-Nachrichten enthalten sind. 
  
Client-Anwendungen k�nnen durch Aufrufen der [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode mit 0 und NULL f�r die Parameter  _cbEntryId_ und  _lpEntryId_ jeweils Ordner den obersten Ebene �ffnen. In den meisten F�llen �ffnen Clientanwendungen jedoch den Satz von Ordnern, die IPM Nachrichten enthalten. 
  
Wenn Sie eine Liste der Ordner in den Nachrichtenspeicher IPM Ordnerstruktur erhalten m�chten, verwenden Sie die folgende Schritte aus:
  
1. Rufen Sie die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)-Methode mithilfe der MAPI-Sitzung auf. 
    
2. Verwenden Sie den resultierenden Nachrichtendatenbankzeiger zum Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md)-Methode für die **PR_IPM_SUBTREE_ENTRYID** ( [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft.
    
3. Rufen Sie die [IMsgStore::OpenEntry](imsgstore-openentry.md)-Methode mit der Eintrags-ID auf, um einen **IMAPIFolder**-Verweis zu erhalten. 
    
4. Rufen Sie die [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Abrufen einer Tabelle der Inhalt des Ordners. 
    
5. Rufen Sie [die QueryRows, um eine Liste der Ordner im Ordner obersten Ebene](imapitable-queryrows.md) . 
    
MAPI-Clients verwenden diese Ordner, um auf andere Ordnerobjekte und Nachrichtenobjekte im Nachrichtenspeicher zuzugreifen. **IMAPIFolder** und die übergeordnete Schnitstelle [IMAPIContainer](imapicontainerimapiprop.md) enthalten die Methoden, die Ihr Nachrichtenspeicheranbieter implementieren muss, um Ordner mit Nachrichtenobjekten aufzufüllen und auf Clientanfragen im Zusammenhang mit Nachrichten zu reagieren.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Ordnern in Nachrichtenspeichern](implementing-folders-in-message-stores.md)

