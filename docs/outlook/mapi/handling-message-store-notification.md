---
title: Behandeln von Nachrichtenspeicherbenachrichtigungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d370603dc7cfc015fe7b2757d1cf0525b3092c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428025"
---
# <a name="handling-message-store-notification"></a>Behandeln von Nachrichtenspeicherbenachrichtigungen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Rufen Sie zum Registrieren für Nachrichtenspeicherbenachrichtigungen entweder die [IMAPISession::Advise-](imapisession-advise.md) oder [die IMsgStore::Advise-Methode](imsgstore-advise.md) auf, und geben Sie im Inhalt des  _lpEntryID-Parameters_ einen Nachrichtenspeicher, einen Ordner oder einen Nachrichteneintragsbezeichner an. Nachrichtenspeicheranbieter unterstützen Objekt- und Tabellenbenachrichtigungen. Ob Sie sich bei bestimmten Nachrichtenspeicherobjekten registrieren, mit der Ordnerhierarchie und den Inhaltstabellen, die diese Objekte beschreiben, oder mit Objekten und Tabellen, hängt von den Benachrichtigungen ab, die Sie erwarten, den Aufrufen, die Sie zum Ausführen von Vorgängen ausführen, und davon, wie der Nachrichtenspeicheranbieter die Benachrichtigung unterstützt. 
  
Da MAPI Flexibilität bei der Unterstützung von Benachrichtigungen durch Anbieter zulässt, sollten Sie beachten, dass Sie nicht immer dieselbe Art von Benachrichtigung als Reaktion auf ein bestimmtes Ereignis von allen Nachrichtenspeicheranbietern erhalten. Einige Nachrichtenspeicheranbieter unterstützen keine Benachrichtigungen. Um zu ermitteln, ob der von Ihnen verwendete Nachrichtenspeicher eine Benachrichtigung unterstützt, suchen Sie in der STORE_NOTIFY_OK -Bit in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft.
  
An einem Ende des Spektrums der Nachrichtenspeicheranbieter, die Benachrichtigungen unterstützen, sind die Anbieter, die "umfangreiche" Benachrichtigungen generieren. Diese Anbieter senden beschreibende Benachrichtigungen für alle registrierten Ratgeberquellen. Am anderen Ende befinden sich die Nachrichtenspeicheranbieter, die eingeschränkte Benachrichtigungen unterstützen. Diese Anbieter senden allgemeine Benachrichtigungen für eine eingeschränkte Anzahl von Ratgeberquellen. 
  
Wenn Sie z. B. eine Nachricht in einen Ordner kopieren, in dem Sie sich registriert haben, um sowohl objektkopierte als auch objekt verschobene Benachrichtigungen zu erhalten, erhalten Sie möglicherweise die objektkopierte Benachrichtigung. Ob Sie sie erhalten, hängt von den
  
- Die Methode, die Sie zum Ausführen der Kopie aufgerufen haben. Dies kann [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)oder [IMAPIProp::CopyProps sein.](imapiprop-copyprops.md)
    
- Implementierung der Kopiermethode durch den Nachrichtenspeicheranbieter.
    
- Gibt an, ob der Nachrichtenspeicheranbieter objekt kopierte Benachrichtigungen in Ordnern unterstützt.
    
Da es keine strengen Richtlinien gibt, die beschreiben, wie Ereignisbenachrichtigungen für Nachrichtenspeicheranbieter implementiert werden, können Clients kein konsistentes Verhalten erwarten. MAPI gibt Empfehlungen zur Implementierung von Ereignisbenachrichtigungen durch Nachrichtenspeicheranbieter, und in der folgenden Tabelle werden diese Empfehlungen aufgeführt. Lesen Sie die Tabelle wie folgt: Nachdem Sie den Vorgang in der ersten Spalte ausführen, erwarten Sie, dass sie eine Benachrichtigung des Typs erhalten, der in der zweiten Spalte aufgeführt ist, wenn Sie sich für diesen Typ mit dem in der dritten Spalte aufgeführten Objekt registriert haben. Nachdem Sie beispielsweise einen Ordner erstellt haben, erhalten Sie eine  _fnevObjectCreated-Benachrichtigung_ nur, wenn Sie sich beim Nachrichtenspeicher für  _fnevObjectCreated-Benachrichtigungen_ registriert haben. 
  
|**Vorgang**|**Ereignistyp**|**Quelle "Beraten"**|
|:-----|:-----|:-----|
|Erstellen eines Ordners  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher  <br/> |
|Löschen eines Ordners  <br/> | _fnevObjectDeleted_ <br/> |Nachrichtenspeicher Gelöschter Ordner  <br/> |
|Verschieben eines Ordners von einem Ordner in einen anderen  <br/> | _fnevObjectMoved_ <br/> |Ordner "Nachrichtenspeicher verschoben"  <br/> |
|Kopieren eines Ordners aus einem Ordner in einen anderen  <br/> | _fnevObjectCopied_ <br/> |Nachrichtenspeicher und kopierter Ordner (keine  _fnevObjectCreated-Benachrichtigung_ für die neue Kopie des Ordners gesendet)  <br/> |
|Ändern in einer berechneten Ordnereigenschaft (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Nachrichtenspeicher Geänderter Ordner (Keine Benachrichtigung an übergeordneten Ordner)  <br/> |
|Erstellen einer Nachricht  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher  <br/> |
|Löschen einer Nachricht, wodurch eine Änderung der Eigenschaft des übergeordneten Ordners **PR_CONTENT_COUNT** wird  <br/> | _fnevObjectDeleted_ <br/> |Nachrichtenspeicher Gelöschte Nachricht  <br/> |
|Verschieben einer Nachricht aus einem Ordner in einen anderen  <br/> | _fnevObjectMoved_ <br/> |Nachrichtenspeicher Verschobene Nachricht  <br/> |
|Kopieren einer Nachricht aus einem Ordner in einen anderen  <br/> | _fnevObjectCopied_ <br/> |Nachrichtenspeicher Kopierte Nachricht (Keine  _fnevObjectCreated-Benachrichtigung_ für neue Kopie der Nachricht)  <br/> |
|Speichern einer Nachricht, wodurch eine Änderung der Eigenschaft des übergeordneten Ordners **PR_CONTENT_COUNT** wird  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher nur beim ersten Speichern  <br/> |
|Speichern einer Nachricht  <br/> | _fnevObjectModified_ <br/> |Nachrichtenspeicher bei speichert nach dem ersten Speichern Geänderte Nachricht (Keine Benachrichtigung an übergeordneten Ordner)  <br/> |
|Abschließen eines Suchvorgangs  <br/> | _fnevSearchComplete_ <br/> |Suchordner des Nachrichtenspeichers  <br/> |
|Neue Nachricht  <br/> | _fnevNewMail_ <br/> |Nachrichtenspeicher  <br/> |
   
> [!NOTE]
> Wenn Sie eine Benachrichtigung zum Ändern eines Objekts [](object_notification.md) erhalten, denken Sie daran, dass der Arrayteil des Eigenschaftstags der OBJECT_NOTIFICATION-Struktur, auf den der _lpNotifications-Parameter_ im **OnNotify-Aufruf** verweist, null sein kann oder nicht. Nachrichtenspeicheranbieter müssen keine Eigenschafteninformationen in dieses Array einfügen, die meisten nicht. Stellen Sie sicher, dass **ihre OnNotify-Methode** den Fall behandeln kann, bei dem  _der lpPropTagArray-Zeiger_ NULL ist. 
  
Aktualisieren Sie für die meisten, wenn nicht alle Objektbenachrichtigungen die Ansicht des betroffenen Ordners oder Ordners.
  

