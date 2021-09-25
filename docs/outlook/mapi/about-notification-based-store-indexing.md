---
title: Informationen zur Notification-Based Store Indizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d00b0b65639786a561830ed50f555b17519aba9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592760"
---
# <a name="about-notification-based-store-indexing"></a>Informationen zur Notification-Based Store Indizierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Speicheranbieter kann angeben, ob der MAPI-Protokollhandler Nachrichten im Speicher durchforstet und indiziert oder ob der Informationsspeicher Benachrichtigungen an den Indexer sendet, wenn Nachrichten indiziert werden sollen. Letzteres wird als benachrichtigungsbasierte Indizierung bezeichnet, und ein Informationsspeicher, der die benachrichtigungsbasierte Indizierung unterstützt, wird als Pusherspeicher bezeichnet.
  
Ein Speicheranbieter, der die benachrichtigungsbasierte Indizierung unterstützt, legt das **STORE_PUSHER_OK** Flag in der **[PR_STORE_SUPPORT_MASK-Eigenschaft](pidtagstoresupportmask-canonical-property.md)** fest. Der MAPI-Protokollhandler oder ein Client kann die **PR_STORE_SUPPORT_MASK** Eigenschaft abrufen, um die Merkmale des Speichers zu bestimmen. 
  
Wenn eine Anlage, ein Ordner oder eine Nachricht indiziert werden soll, generiert der Speicheranbieter einen MAPI Uniform Resource Locator (URL), der das zu indizierende Objekt identifiziert und an den Indexer sendet. Diese MAPI-URL ist in Unicode codiert und muss das Objekt eindeutig für den MAPI-Protokollhandler identifizieren. Weitere Informationen zu MAPI-URLs finden Sie unter [Informationen zu MAPI-URLs für Notification-Based-Indizierung.](about-mapi-urls-for-notification-based-indexing.md)
  
Da ein Indexer nicht immer alles indiziert, bevor ein Herunterfahren in einem Pusherspeicher erfolgt, muss der Pusherspeicher beibehalten werden, was verschoben werden muss. Wenn ein Speicheranbieter eine Benachrichtigung über ein Objekt sendet, das indiziert werden muss, gibt er den Benachrichtigungstyp **fnevIndexing** im **ulEventType-Element** der **[NOTIFICATION-Struktur an.](notification.md)** Das **info**-Mitglied der **NOTIFICATION**-Struktur enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)**-Struktur. Der Speicheranbieter identifiziert den **[](pidtagsearchownerid-canonical-property.md)** Prozess in der PR_SEARCH_OWNER_ID-Eigenschaft. Außerdem wird der Prozess in der [INDEX_SEARCH_PUSHER_PROCESS Struktur](index_search_pusher_process.md) identifiziert und diese Informationen als Teil des **PbEventParameters-Elements** der **EXTENDED_NOTIFICATION-Struktur** übergeben. Wenn der Prozess heruntergefahren wird oder abstürzt, kann der MAPI-Protokollhandler dies sofort erkennen und die Indizierung des Pusherspeichers beenden. 
  
## <a name="see-also"></a>Siehe auch



[Informationen zur Speicher-API](about-the-store-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

