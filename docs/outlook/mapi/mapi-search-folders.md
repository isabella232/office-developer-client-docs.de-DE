---
title: MAPI-Suchordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 26ad19b28d70fb7f68115bc701536002f0c5276b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610167"
---
# <a name="mapi-search-folders"></a>MAPI-Suchordner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria�� rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed. 
  
 **SetSearchCriteria** identifies the messages that match the specified restriction. The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder. When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table. Contents tables for search-results folders contain the same columns as contents tables for generic folders. Bei Suchergebnisordnern gibt die **Eigenschaft PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) jedoch den Eintragsbezeichner des Ordners an, in dem sich die verknüpfte Nachricht befindet. Search-results folders are not considered parent folders.
  
Suchergebnisse Ordner haben die folgenden Einschr�nkungen:
  
- Durch einen Aufruf von **SetSearchCriteria** ist die einzige M�glichkeit, den Inhalt eines Ordners-Ergebnisse ge�ndert werden k�nnen. Weitere Informationen zur Implementierung von **SetSearchCriteria** finden Sie unter Knowledge Base-Artikel [260322: wie auf Suchordner mit der Methode SetSearchCriteria](https://go.microsoft.com/fwlink/?LinkId=123603).
    
- Nachrichten werden nicht in Suchergebnissen Ordner kopiert oder verschoben.
    
- Suchergebnisse Ordner k�nnen keine Unterordner enthalten. 
    
- Clients einem Suchergebnisse Ordner des Betreffs einer Suche nicht m�glich.
    
Es ist jedoch m�glich, zum �ndern der Eigenschaften eines Ordners Suchergebnisse und verwenden, um eine Nachricht zu l�schen. Wenn eine Nachricht aus einem Suchergebnisse Ordner gel�scht wird, wird es aus dem Ordner realen tats�chlich gel�scht. L�schen den Suchergebnisse Ordner selbst haben jedoch keine Auswirkungen auf die Nachrichten innerhalb; bleiben sie in ihren generischen Ordnern.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

