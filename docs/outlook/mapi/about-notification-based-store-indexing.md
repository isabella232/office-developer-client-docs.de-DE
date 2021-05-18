---
title: Informationen Notification-Based Store-Indizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409174"
---
# <a name="about-notification-based-store-indexing"></a>Informationen Notification-Based Store-Indizierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Speicheranbieter kann angeben, ob der MAPI-Protokollhandler Nachrichten im Speicher durchforstet und indiziert oder ob der Speicher Benachrichtigungen an den Indexer sendet, wenn Nachrichten indiziert werden sollen. Letzteres wird als benachrichtigungsbasierte Indizierung bezeichnet, und ein Speicher, der die benachrichtigungsbasierte Indizierung unterstützt, wird als Pushspeicher bezeichnet.
  
Ein Speicheranbieter, der die benachrichtigungsbasierte Indizierung unterstützt, legt **das** STORE_PUSHER_OK in **[der](pidtagstoresupportmask-canonical-property.md)** PR_STORE_SUPPORT_MASK fest. Der MAPI-Protokollhandler oder ein Client kann die **PR_STORE_SUPPORT_MASK,um** die Merkmale des Speichers zu bestimmen. 
  
Wenn eine Anlage, ein Ordner oder eine Nachricht indiziert werden soll, generiert der Speicheranbieter einen MAPI Uniform Resource Locator (URL), der das zu indizierte Objekt identifiziert und an den Indexer sendet. Diese MAPI-URL ist in Unicode codiert und muss das Objekt für den MAPI-Protokollhandler eindeutig identifizieren. Weitere Informationen zu MAPI-URLs finden Sie unter [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).
  
Da ein Indexer nicht immer alles indizieren kann, bevor ein Herunterfahren in einem Pushspeicher stattfindet, muss der Pushspeicher beibehalten, was pusht werden muss. Wenn ein Speicheranbieter eine Benachrichtigung über ein Objekt sendet, das indiziert werden muss, gibt er den Benachrichtigungstyp **fnevIndexing** im **ulEventType-Element** der **[NOTIFICATION-Struktur](notification.md)** an. Das **info**-Mitglied der **NOTIFICATION**-Struktur enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)**-Struktur. Der Speicheranbieter identifiziert den **[](pidtagsearchownerid-canonical-property.md)** Prozess in der PR_SEARCH_OWNER_ID-Eigenschaft. Außerdem wird der Prozess in der INDEX_SEARCH_PUSHER_PROCESS [identifiziert](index_search_pusher_process.md) und diese Informationen als Teil des **pbEventParameters-Mitglieds** der EXTENDED_NOTIFICATION **werden.** Wenn der Prozess heruntergefahren oder abstürzt, kann der MAPI-Protokollhandler dies sofort erkennen und die Indizierung des Pushspeichers beenden. 
  
## <a name="see-also"></a>Siehe auch



[Informationen zur Speicher-API](about-the-store-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

