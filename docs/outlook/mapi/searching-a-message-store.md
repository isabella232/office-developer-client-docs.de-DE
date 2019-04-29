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
  
Client Anwendungen können einen oder mehrere Ordner durchsuchen, die nach Nachrichten suchen, die den Suchkriterien entsprechen. Die einfachste Suchmethode umfasst das Anwenden einer Einschränkung zum Definieren von Kriterien und das Platzieren der Ergebnisse in einem Suchergebnisordner, der explizit für diese Suche oder für eine vorherige Suche erstellt wurde. Diese Technik wird nicht von allen Nachrichten speichern unterstützt. 

Um zu bestimmen, ob der von Ihnen verwendete Nachrichtenspeicher mithilfe von Suchergebnis Ordnern unterstützt, rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode auf, um die **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft abzurufen. Wenn das STORE_SEARCH_OK-Flag festgelegt ist, wird die Suche unterstützt. Wenn Sie nicht festgelegt ist, benötigen Sie einen alternativen Ansatz wie die manuelle Überprüfung der Zielordner.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>So durchsuchen Sie einen oder mehrere Ordner in einem Nachrichtenspeicher
  
1. Wenn Sie einen Suchergebnisordner aus einer früheren Suche haben, fahren Sie mit Schritt 2 fort. Andernfalls können Sie einen Suchergebnisordner erstellen:
    
    1. Rufen Sie die Eintrags-ID für den Suchergebnis-Stammordner ab, indem Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers aufrufen und **PR_FINDER_ENTRYID** ([pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md)) anfordern.
        
    2. Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) auf, um den durch PR_FINDER_ENTRYID dargestellten Ordner zu öffnen. 
        
    3. Rufen Sie die [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) -Methode des Ordners auf, um einen Ordner mit Suchergebnissen mit dem FOLDER_SEARCH-Kennzeichen Satz zu erstellen. 
    
2. Erstellen Sie eine Einschränkung für Ihre Suchkriterien. 
    
3. Erstellen Sie ein Array von Eintrags Bezeichnern, die die zu durchsuchenden Ordner darstellen. Dieser Schritt ist nicht erforderlich, wenn der Ordner Suchergebnisse zuvor verwendet wurde und Sie die gleichen Ordner durchsuchen möchten.
    
4. Rufen Sie die [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode des Suchergebnis Ordners auf, und zeigen Sie _lpContainerList_ auf das Array Eintrags-ID und _lpRestriction_ auf die Einschränkung. 
    
5. Wenn Sie sich mit dem Nachrichtenspeicher für vollständige Benachrichtigungen bei der Suche registriert haben, warten Sie, bis die Benachrichtigung eingeht.
    
6. Zeigen Sie die Ergebnisse der Suche an, indem Sie die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode des Search-results-Ordners aufrufen, um auf die Inhaltstabelle zuzugreifen. 
    
7. Rufen Sie die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode der Inhaltstabelle auf, um die Nachrichten abzurufen, die den Suchkriterien entsprechen. 
    

