---
title: Über den API-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 31aff61ec5868b0f1e9ab34d498b2e8175519f0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791254"
---
# <a name="about-the-store-api"></a>Über den API-Speicher

  
  
**Betrifft**: Outlook 
  
Die speichern-API bietet verschiedene Speicherfunktionalität zum Speichern von Anbietern. Es bietet die folgenden Definitionen Datentypen, Eigenschaften und Schnittstellen.
  
Definitionen:
  
- [Konstanten für den API-Speicher](mapi-constants.md)
    
Datentypen:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Benannte Eigenschaften:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Ordnergröße Server anzeigen](display-server-folder-sizes-property.md)**
    
- **[Ausblenden der Besprechung Update-Option](hide-meeting-update-option-property.md)**
    
- **[Stellen Sie Store Typ Private](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Anbieter, die nicht über die Funktionalität dieser benannten Eigenschaften erfordern können einfach ignoriert werden sollen und nicht Support in der **IMAPIProp** -Schnittstelle implementieren. Da diese Eigenschaften in Microsoft Outlook 2003 Service Pack 1 beginnende verfügbar sind, hat einen Speicher in einer früheren Version von Microsoft Outlook hinzugefügt keine Auswirkung. Wenn sie nicht vorhanden sind oder deren Wert **false**ist, werden sie ignoriert. 
  
Eigenschaften:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Schnittstellen:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registrieren Speicher für die Indizierung

Der MAPI-Protokollhandler überprüft die Windows-Registrierung für Geschäfte, die indiziert werden soll für die Suche. Speicheranbieter, die indiziert werden soll, müssen in der Windows-Registrierung registriert werden. Weitere Informationen zum Registrieren von Anbietern für die Indizierung in Outlook 2013 oder Outlook 2010 finden Sie unter [Informationen zum Registrieren-Speicher für die Indizierung](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Speichert die Indizierung

MAPI-Anbieter können wahlweise den MAPI-Protokollhandler zum Durchforsten und Indizieren von Nachrichten im Speicher zulassen oder Senden von Benachrichtigungen an die Indizierung, nur, wenn Nachrichten indiziert werden kann. Weitere Informationen zu Benachrichtigungen-basierte Indizierung finden Sie unter [About Notification-Based Store indizieren](about-notification-based-store-indexing.md).
  

