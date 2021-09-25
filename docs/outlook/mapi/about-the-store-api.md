---
title: Informationen zur Speicher-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: deba8ea99e53d3bc20267d4beb92952af14adfaa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592744"
---
# <a name="about-the-store-api"></a>Informationen zur Speicher-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Store-API bietet verschiedene Speicherfunktionen zum Speichern von Anbietern. Es stellt die folgenden Definitionen, Datentypen, Eigenschaften und Schnittstellen bereit.
  
Definitionen:
  
- [Konstanten für die Store-API](mapi-constants.md)
    
Datentypen:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Benannte Eigenschaften:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Anzeigeserverordnergrößen](display-server-folder-sizes-property.md)**
    
- **[Option "Besprechungsupdate ausblenden"](hide-meeting-update-option-property.md)**
    
- **[Make Store Type Private](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Store Anbieter, die keine der von diesen benannten Eigenschaften angebotenen Funktionen benötigen, können diese einfach ignorieren und keine Unterstützung in der **IMAPIProp-Schnittstelle** implementieren. Da diese Eigenschaften ab Microsoft Outlook 2003 Service Pack 1 bereitgestellt werden, hat das Hinzufügen zu einem Store in einer früheren Version von Microsoft Outlook keine Auswirkungen. Sie werden ignoriert, wenn sie nicht vorhanden sind oder wenn ihr Wert **falsch** ist. 
  
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

Der MAPI-Protokollhandler überprüft die Windows-Registrierung auf Speicher, die für Suchzwecke indiziert werden sollen. Store Anbieter, die indiziert werden sollen, müssen in der Windows Registrierung registriert werden. Weitere Informationen zum Registrieren von Speicheranbietern für die Indizierung in Outlook 2013 oder Outlook 2010 finden Sie unter ["Registrieren von Stores für die Indizierung".](about-registering-stores-for-indexing.md)
  
## <a name="indexing-stores"></a>Indizierungsspeicher

MAPI-Speicheranbieter können festlegen, dass der MAPI-Protokollhandler Nachrichten im Speicher durchforsten und indizieren kann, oder Benachrichtigungen nur dann an den Indexer senden, wenn Nachrichten indiziert werden sollen. Weitere Informationen zur benachrichtigungsbasierten Indizierung finden Sie unter [Info zu Notification-Based Store Indizierung.](about-notification-based-store-indexing.md)
  

