---
title: Durchsuchen eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8ed987a558b90c22682fd050bf9d1e456eda964f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591171"
---
# <a name="searching-a-message-store"></a>Durchsuchen eines Nachrichtenspeichers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen können einen oder mehrere Ordner durchsuchen, die nach Nachrichten suchen, die den Suchkriterien entsprechen. Die einfachste Suchmethode besteht darin, eine Einschränkung anzuwenden, um Kriterien zu definieren und die Ergebnisse in einem Suchergebnisordner zu platzieren, der explizit für diese Suche oder für eine vorherige Suche erstellt wurde. Nicht alle Nachrichtenspeicher unterstützen diese Technik. 

Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) auf, um festzustellen, ob der von Ihnen verwendete Nachrichtenspeicher die Verwendung von Suchergebnisordnern unterstützt, um die **\_ PR-STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft abzurufen. Wenn das STORE_SEARCH_OK-Kennzeichen festgelegt ist, wird die Suche unterstützt. Wenn sie nicht festgelegt ist, benötigen Sie einen alternativen Ansatz, z. B. die manuelle Überprüfung der Zielordner.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>So durchsuchen Sie einen oder mehrere Ordner in einem Nachrichtenspeicher
  
1. Wenn Sie über einen Suchergebnisordner aus einer vorherigen Suche verfügen, fahren Sie mit Schritt 2 fort. Andernfalls zum Erstellen eines Suchergebnisordners:
    
    1. Rufen Sie den Eintragsbezeichner für den Stammordner der Suchergebnisse ab, indem Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers aufrufen und **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) anfordern.
        
    2. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) auf, um den durch PR_FINDER_ENTRYID dargestellten Ordner zu öffnen. 
        
    3. Rufen Sie die [IMAPIFolder::CreateFolder-Methode](imapifolder-createfolder.md) des Ordners auf, um einen Suchergebnisordner mit festgelegter FOLDER_SEARCH Zu erstellen. 
    
2. Erstellen Sie eine Einschränkung, um Ihre Suchkriterien zu speichern. 
    
3. Erstellen Sie ein Array von Eintragsbezeichnern, die die zu durchsuchenden Ordner darstellen. Dieser Schritt ist nicht erforderlich, wenn der Suchergebnisordner zuvor verwendet wurde und Sie dieselben Ordner durchsuchen möchten.
    
4. Rufen Sie die [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) des Suchergebnissenordners auf, und verweisen Sie  _lpContainerList_ auf das Eintragsbezeichnerarray und  _lpRestriction_ auf die Einschränkung. 
    
5. Wenn Sie sich für die Suche nach vollständigen Benachrichtigungen beim Nachrichtenspeicher registriert haben, warten Sie, bis die Benachrichtigung eintrifft.
    
6. Zeigen Sie die Ergebnisse der Suche an, indem Sie die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Suchergebnisordners aufrufen, um auf das Inhaltsverzeichnis zuzugreifen. 
    
7. Rufen Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) des Inhaltsverzeichnisses auf, um die Nachrichten abzurufen, die die Suchkriterien erfüllen. 
    

