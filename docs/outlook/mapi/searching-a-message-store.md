---
title: Durchsuchen eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426037"
---
# <a name="searching-a-message-store"></a>Durchsuchen eines Nachrichtenspeichers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen können einen oder mehrere Ordner durchsuchen, die nach Nachrichten suchen, die den Suchkriterien entsprechen. Die unkomplizierteste Suchmethode umfasst das Anwenden einer Einschränkung zum Definieren von Kriterien und das Platzieren der Ergebnisse in einem Suchergebnisordner, der explizit für diese Suche oder für eine vorherige Suche erstellt wurde. Nicht alle Nachrichtenspeicher unterstützen diese Technik. 

Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) auf, um zu bestimmen, ob der von Ihnen verwendete Nachrichtenspeicher die Verwendung von Suchergebnissen unterstützt, um die **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft abzurufen. Wenn das STORE_SEARCH_OK festgelegt ist, wird die Suche unterstützt. Wenn sie nicht festgelegt ist, benötigen Sie einen alternativen Ansatz, z. B. die manuelle Überprüfung der Zielordner.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>So durchsuchen Sie einen oder mehrere Ordner in einem Nachrichtenspeicher
  
1. Wenn Sie über einen Suchergebnisordner aus einer vorherigen Suche verfügen, fahren Sie mit Schritt 2 fort. Andernfalls, um einen Suchergebnisordner zu erstellen:
    
    1. Rufen Sie die Eintrags-ID für den Stammordner der Suchergebnisse ab, indem Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers aufrufen und PR_FINDER_ENTRYID **(** [PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) anfordern.
        
    2. Rufen [Sie IMsgStore::OpenEntry auf,](imsgstore-openentry.md) um den durch die Datei dargestellten Ordner PR_FINDER_ENTRYID. 
        
    3. Rufen Sie die [IMAPIFolder::CreateFolder-Methode](imapifolder-createfolder.md) des Ordners auf, um einen Suchergebnisordner mit dem FOLDER_SEARCH zu erstellen. 
    
2. Erstellen Sie eine Einschränkung, um Ihre Suchkriterien zu halten. 
    
3. Erstellen Sie ein Array von Eintragsbezeichnern, die die zu durchsuchenden Ordner darstellen. Dieser Schritt ist nicht erforderlich, wenn der Suchergebnisordner bereits verwendet wurde und Sie dieselben Ordner durchsuchen möchten.
    
4. Rufen Sie die [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) des Suchergebnisordners auf, und zeigen Sie  _lpContainerList_ auf das Eintragsbezeichnerarray und  _lpRestriction_ auf die Einschränkung. 
    
5. Wenn Sie sich für die Suche mit vollständigen Benachrichtigungen beim Nachrichtenspeicher registriert haben, warten Sie, bis die Benachrichtigung eintrifft.
    
6. Zeigen Sie die Ergebnisse der Suche an, indem Sie die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Suchergebnisordners aufrufen, um auf die Inhaltstabelle zu zugreifen. 
    
7. Rufen Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) der Inhaltstabelle auf, um die Nachrichten abzurufen, die den Suchkriterien entsprechen. 
    

