---
title: Suchen eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 90ed7da43d7f9e5e8b5f3024f1eee99a2d7a2b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795471"
---
# <a name="searching-a-message-store"></a>Suchen eines Nachrichtenspeichers

**Betrifft**: Outlook 
  
Clientanwendungen können Suchen über einen oder mehrere Ordner suchen Sie nach Nachrichten, die den Suchkriterien entsprechen. Die einfachste Suchverfahren umfasst das Anwenden einer Einschränkung zum Definieren von Kriterien und platzieren die Ergebnisse in einem Ordner-Ergebnisse für diese Suche oder bei einer vorherigen Suche explizit erstellt. Nicht alle Nachrichtenspeicher unterstützt diese Technik. 

Bestimmen unterstützt, unabhängig davon, ob die Nachrichtenspeicher Sie verwenden die Verwendung von Suchergebnissen Ordner, rufen Sie seine [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der **PR\_STORE_SUPPORT_MASK** -Eigenschaft ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Wenn das Flag STORE_SEARCH_OK festgelegt ist, wird die Suche unterstützt. Wenn es nicht festgelegt ist, benötigen Sie eine alternative Methode wie manuelle Überprüfung der Zielordner.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Suchen Sie einen oder mehrere Ordner in einem Nachrichtenspeicher
  
1. Wenn Sie einen Ordner Suchergebnisse aus einem früheren Suchvorgang haben, fahren Sie mit Schritt 2 fort. Andernfalls, erstellen Sie einen Ordner-Ergebnisse:
    
    1. Rufen Sie die Eintrags-ID für den Stammordner-Ergebnisse der Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode aufrufen und Anfordern einer **PR_FINDER_ENTRYID** ([PidTagFinderEntryId ab](pidtagfinderentryid-canonical-property.md)).
        
    2. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) zum Öffnen des Ordners durch PR_FINDER_ENTRYID dargestellt. 
        
    3. Rufen Sie den Ordner [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) -Methode zum Erstellen eines Suchergebnisse-Ordners mit der FOLDER_SEARCH-Flag. 
    
2. Erstellen Sie eine Einschränkung, um Ihre Suchkriterien zu halten. 
    
3. Erstellen Sie ein Array von Eintragsbezeichner, die den Ordner für die Suche darstellen. Dieser Schritt ist nicht erforderlich, wenn der Suchergebnisse Ordner vor verwendet wurde und Sie die gleichen Ordner suchen möchten.
    
4. Rufen Sie den Suchergebnisse Ordner [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode, die Eintrags-ID-Array und _LpRestriction_ die Beschränkung auf _LpContainerList_ . 
    
5. Wenn Sie für die Suche abgeschlossen Benachrichtigungen mit dem Nachrichtenspeicher registriert haben, warten Sie auf die Benachrichtigung eingeht.
    
6. Zeigen Sie die Ergebnisse der Suche durch Aufrufen der Suchergebnisse des Ordners [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode zum Zugriff auf die Inhaltstabelle an. 
    
7. Rufen Sie den Inhalt [der Tabelle QueryRows Abrufen die Nachrichten, die die Suchkriterien erfüllen](imapitable-queryrows.md) . 
    

