---
title: Informationen zur Speicher-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405555"
---
# <a name="about-the-store-api"></a>Informationen zur Speicher-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Store-API stellt verschiedene Speicherfunktionen für Speicheranbieter bereit. Es enthält die folgenden Defintions, Datentypen, Eigenschaften und Schnittstellen.
  
Definitionen:
  
- [Konstanten für die Store-API](mapi-constants.md)
    
Datentypen:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Benannte Eigenschaften:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Größe des Anzeigeserverordners](display-server-folder-sizes-property.md)**
    
- **[Option zum Ausblenden von Besprechungsupdates](hide-meeting-update-option-property.md)**
    
- **[Make Store Type Private](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Store, die keine der Funktionen dieser benannten Eigenschaften benötigen, können sie einfach ignorieren und keine Unterstützung in der **IMAPIProp-Schnittstelle** implementieren. Da diese Eigenschaften ab Microsoft Outlook 2003 Service Pack 1 bereitgestellt werden, hat das Hinzufügen zu einem Store in einer früheren Version von Microsoft Outlook keine Auswirkung. Sie werden ignoriert, wenn sie nicht vorhanden sind oder ihr Wert false **ist.** 
  
Eigenschaften:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Schnittstellen:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registrieren von Informationsspeichern für die Indizierung

Der MAPI-Protokollhandler überprüft die Windows für Speicher, die zu Suchzwecken indiziert werden sollen. Store, die indiziert werden möchten, müssen in der Registrierung Windows werden. Weitere Informationen zum Registrieren von Speicheranbietern für die Indizierung in Outlook 2013 oder Outlook 2010 finden Sie unter [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Indizierungsspeicher

MAPI-Speicheranbieter können festlegen, dass der MAPI-Protokollhandler Nachrichten im Speicher durchforstet und indiziert oder Benachrichtigungen nur dann an den Indexer sendet, wenn Nachrichten indiziert werden sollen. Weitere Informationen zur Benachrichtigungsbasierten Indizierung finden Sie unter [Informationen Notification-Based Store Indizierung](about-notification-based-store-indexing.md).
  

