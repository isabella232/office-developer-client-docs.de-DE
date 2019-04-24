---
title: Informationen zu Benachrichtigungs basierter Speicher Indizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322134"
---
# <a name="about-notification-based-store-indexing"></a>Informationen zu Benachrichtigungs basierter Speicher Indizierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Speicheranbieter kann angeben, ob der MAPI-Protokoll Handler Nachrichten im Speicher durchforstet und indiziert, oder ob der Informationsspeicher Benachrichtigungen an den Indexer sendet, wenn Nachrichten indiziert werden sollen. Letztere wird als Benachrichtigungs basierte Indizierung bezeichnet, und ein Speicher, der die Benachrichtigungs basierte Indizierung unterstützt, wird als Pusher-Speicher bezeichnet.
  
Ein Informationsspeicher Anbieter, der die Benachrichtigungs basierte Indizierung unterstützt, legt das **STORE_PUSHER_OK** -Flag in der **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** -Eigenschaft fest. Der MAPI-Protokoll Handler oder ein Client kann die **PR_STORE_SUPPORT_MASK** -Eigenschaft abrufen, um die Eigenschaften des Speichers zu bestimmen. 
  
Wenn eine Anlage, ein Ordner oder eine Nachricht indiziert werden soll, generiert der Speicheranbieter einen MAPI-URL (Uniform Resource Locator), der das zu indizierende Objekt identifiziert und es an den Indexer sendet. Diese MAPI-URL ist in Unicode codiert und muss das Objekt eindeutig dem MAPI-Protokoll Handler zuordnen. Weitere Informationen zu MAPI-URLs finden Sie unter [Informationen zu MAPI-URLs für die Benachrichtigungs basierte Indizierung](about-mapi-urls-for-notification-based-indexing.md).
  
Da ein Indexer nicht immer alles indizieren kann, bevor ein Herunterfahren in einem Pusher-Speicher erfolgt, muss der Pusher-Speicher beibehalten, was verschoben werden muss. Wenn ein Informationsspeicher Anbieter eine Benachrichtigung über ein Objekt sendet, das indiziert werden muss, gibt es den Benachrichtigungstyp **fnevIndexing** im **ulEventType** -Element der **[Benachrichtigungs](notification.md)** Struktur an. Das **info**-Mitglied der **NOTIFICATION**-Struktur enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)**-Struktur. Der Informationsspeicher Anbieter identifiziert den Prozess in der **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** -Eigenschaft. Außerdem wird der Prozess in der [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) -Struktur identifiziert, und diese Informationen werden als Teil des **pbEventParameters** -Elements der **EXTENDED_NOTIFICATION** -Struktur übergeben. Wenn der Prozess heruntergefahren oder abstürzt, kann der MAPI-Protokoll Handler sofort feststellen, dass die Indizierung des Pusher-Speichers beendet wird. 
  
## <a name="see-also"></a>Siehe auch



[Informationen zur Speicher-API](about-the-store-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

