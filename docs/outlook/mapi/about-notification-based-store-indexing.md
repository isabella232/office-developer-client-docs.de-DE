---
title: Informationen zum benachrichtigungsbasierten Indizieren von Stores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791224"
---
# <a name="about-notification-based-store-indexing"></a>Informationen zum benachrichtigungsbasierten Indizieren von Stores

  
  
**Betrifft**: Outlook 
  
Ein MAPI-Anbieter kann angeben, ob der MAPI-Protokollhandler Durchforstungen und Indizes im Speicher Nachrichten oder gibt an, ob der Speicher sendet Benachrichtigungen die Indizierung sind Nachrichten indiziert werden. Da letztere als Benachrichtigung-basierte Indizierung bezeichnet wird, und ein Speicher, der Benachrichtigung-basierte Indizierung unterstützt, ist ein bekanntes als Pusher Speicher.
  
Ein Store-Anbieter, der Benachrichtigung-basierte Indizierung legt das Flag **STORE_PUSHER_OK** in die **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** -Eigenschaft unterstützt. Der MAPI-Protokollhandler oder einen Client kann die **PR_STORE_SUPPORT_MASK** -Eigenschaft zum Ermitteln der Merkmale des Speichers abrufen. 
  
Wenn eine Anlage, Ordner oder eine Nachricht zu indizierenden vorhanden ist, Speicheranbieter generiert ein MAPI-Uniform Resource Locator (URL) zur Identifizierung des Objekts für die Indizierung und sendet ihn an die Indizierung. Der MAPI-URL ist in Unicode codiert und muss eindeutig das Objekt, das den MAPI-Protokollhandler. Weitere Informationen zu MAPI-URLs finden Sie unter [Informationen zu MAPI-URLs für Benachrichtigung-basierte Indizierung](about-mapi-urls-for-notification-based-indexing.md).
  
Da Indexer immer alles nicht indiziert werden vor dem Herunterfahren in einem Speicher Pusher, muss Pusher Speicher beibehalten was abgelegt werden muss. Wenn ein Anbieter zu einem Objekt eine Benachrichtigung, die indiziert werden soll sendet, gibt die Benachrichtigung Typ **FnevIndexing** im **UlEventType** -Member der Struktur **[Benachrichtigung](notification.md)** an. Der **Info** -Member der Struktur **Benachrichtigung** enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)** -Struktur. Speicheranbieter identifiziert den Prozess in der **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** -Eigenschaft. Auch identifiziert den Prozess der [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) -Struktur, und übergibt diese Informationen im Rahmen der **PbEventParameters** Mitglied der **EXTENDED_NOTIFICATION** -Struktur. Wenn der Prozess heruntergefahren wird oder stürzt ab, wird der MAPI-Protokollhandler werden sofort zu erkennen, und beenden Sie den Pusher Speicher Indizierung. 
  
## <a name="see-also"></a>Siehe auch



[Informationen zur Store-API](about-the-store-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

