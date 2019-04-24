---
title: Informationen zur Speicher-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321749"
---
# <a name="about-the-store-api"></a>Informationen zur Speicher-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Informationsspeicher-API bietet Speicheranbietern verschiedene Speicherfunktionen. Es bietet die folgenden Definitionen, Datentypen, Eigenschaften und Schnittstellen.
  
Definitionen:
  
- [Konstanten für die Speicher-API](mapi-constants.md)
    
Datentypen:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Benannte Eigenschaften:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Größe des Anzeige Server Ordners](display-server-folder-sizes-property.md)**
    
- **[Option "Besprechungs Update ausblenden"](hide-meeting-update-option-property.md)**
    
- **[Speichertyp als privat festlegen](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Speicheranbieter, die keine der von diesen benannten Eigenschaften angebotenen Funktionen erfordern, können diese einfach ignorieren und keine Unterstützung in der **IMAPIProp** -Schnittstelle implementieren. Da diese Eigenschaften ab Microsoft Outlook 2003 Service Pack 1 bereitgestellt werden, hat das Hinzufügen zu einem Speicher in einer früheren Version von Microsoft Outlook keine Auswirkungen. Sie werden ignoriert, wenn Sie nicht vorhanden sind oder ihr Wert **false**ist. 
  
Eigenschaften:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Schnittstellen:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registrieren von Speichern für die Indizierung

Der MAPI-Protokoll Handler überprüft die Windows-Registrierung auf Speicher, die für Suchzwecke indiziert werden sollen. Speicheranbieter, die indiziert werden sollen, müssen in der Windows-Registrierung registriert werden. Weitere Informationen zum Registrieren von Speicheranbietern für die Indizierung in Outlook 2013 oder Outlook 2010 finden Sie unter Informationen [zum Registrieren](about-registering-stores-for-indexing.md)von Speicher für die Indizierung.
  
## <a name="indexing-stores"></a>Indexspeicher

MAPI-Speicheranbieter können festlegen, dass der MAPI-Protokoll Handler Nachrichten im Speicher Crawlen und indizieren soll, oder Benachrichtigungen an den Indexer senden, wenn Nachrichten indiziert werden sollen. Weitere Informationen zur Benachrichtigungen-basierten Indizierung finden Sie unter [Informationen zu Benachrichtigungs basiertEr Speicher Indizierung](about-notification-based-store-indexing.md).
  

