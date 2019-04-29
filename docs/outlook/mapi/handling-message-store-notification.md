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
  
Wenn Sie sich für Nachrichtenspeicher Benachrichtigungen registrieren möchten, rufen Sie die [IMAPISession:: Advise](imapisession-advise.md) -oder [IMsgStore:: Advise](imsgstore-advise.md) -Methode auf, und geben Sie im Inhalt des _lpEntryID_ -Parameters einen Nachrichtenspeicher, einen Ordner oder eine Nachrichten Eintrags-ID an. Nachrichtenspeicher Anbieter unterstützen sowohl Objekt-als auch Tabellen Benachrichtigungen. Unabhängig davon, ob Sie sich mit bestimmten Nachrichtenspeicher Objekten registrieren, mit den Tabellenhierarchien und Inhaltsverzeichnissen, die diese Objekte beschreiben, oder mit beiden Objekten und Tabellen hängt von den erwarteten Benachrichtigungen ab, welche Anrufe Sie zur Durchführung von Vorgängen vornehmen und wie der Nachrichtenspeicher Anbieter unterstützt Benachrichtigungen. 
  
Da MAPI die Flexibilität in der Art der Unterstützung von Anbietern von Benachrichtigungen ermöglicht, müssen Sie beachten, dass Sie nicht immer dieselbe Art von Benachrichtigung als Reaktion auf ein bestimmtes Ereignis von allen Nachrichtenspeicher Anbietern erhalten. Einige Nachrichtenspeicher Anbieter unterstützen keine Benachrichtigungen. Um zu ermitteln, ob der verwendete Nachrichtenspeicher die Benachrichtigung unterstützt, suchen Sie nach dem STORE_NOTIFY_OK-Bit in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft.
  
An einem Ende des Spektrums der Nachrichtenspeicher Anbieter, die Benachrichtigungen unterstützen, handelt es sich um Anbieter, die "Rich"-Benachrichtigungen generieren. Diese Anbieter senden beschreibende Benachrichtigungen für alle registrierten Advise-Quellen. Am anderen Ende befinden sich die Nachrichtenspeicher Anbieter, die eingeschränkte Benachrichtigungen unterstützen. Diese Anbieter senden allgemeine Benachrichtigungen für eine eingeschränkte Anzahl von Advise-Quellen. 
  
Wenn Sie beispielsweise eine Nachricht in einen Ordner kopieren, für den Sie sowohl kopierte Objekte als auch verschobene Objekte erhalten haben, können Sie das Objekt als Kopie der Benachrichtigung erhalten oder nicht. Ob Sie Sie erhalten, hängt von folgenden Themen ab:
  
- Die Methode, die Sie zum Ausführen der Kopie aufgerufen haben. Dies kann [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIProp:: CopyTo](imapiprop-copyto.md)oder [IMAPIProp:: CopyProps](imapiprop-copyprops.md)sein.
    
- Wie der Nachrichtenspeicher Anbieter die Copy-Methode implementiert.
    
- Gibt an, ob der Nachrichtenspeicher Anbieterobjekt kopierte Benachrichtigungen für Ordner unterstützt.
    
Da es keine strengen Richtlinien gibt, die beschreiben, wie Ereignisbenachrichtigungen für Nachrichtenspeicher Anbieter implementiert werden, können Clients kein konsistentes Verhalten erwarten. MAPI gibt Empfehlungen dazu ab, wie Nachrichtenspeicher Anbieter Ereignisbenachrichtigungen implementieren, und in der folgenden Tabelle werden diese Empfehlungen beschrieben. Lesen Sie die Tabelle wie folgt: Wenn Sie den Vorgang in der ersten Spalte ausgeführt haben, erwarten Sie, dass Sie eine Benachrichtigung über den in der zweiten Spalte aufgeführten Typ erhalten, wenn Sie sich für diesen Typ mit dem in der dritten Spalte aufgeführten Objekt registriert haben. Wenn Sie beispielsweise einen Ordner erstellt haben, erhalten Sie nur dann eine _fnevObjectCreated_ -Benachrichtigung, wenn Sie sich für _fnevObjectCreated_ -Benachrichtigungen mit dem Nachrichtenspeicher registriert haben. 
  
|**Vorgang**|**Ereignistyp**|**Quelle beraten**|
|:-----|:-----|:-----|
|Erstellen eines Ordners  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher  <br/> |
|Löschen eines Ordners  <br/> | _fnevObjectDeleted_ <br/> |Gelöschter Nachrichtenspeicher Ordner  <br/> |
|Verschieben eines Ordners aus einem Ordner in einen anderen  <br/> | _fnevObjectMoved_ <br/> |Verschobener Nachrichtenspeicher Ordner  <br/> |
|Kopieren eines Ordners aus einem Ordner in einen anderen  <br/> | _fnevObjectCopied_ <br/> |Nachrichtenspeicher und kopierter Ordner (für die neue Kopie des Ordners wurde keine _fnevObjectCreated_ -Benachrichtigung gesendet)  <br/> |
|Änderung in einer Eigenschaft des berechneten Ordners (**PR_SUBFOLDERS** ([Pidtagsubfolders (](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([pidtagcontentunreadcount (](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([pidtagcontentcount (](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Nachrichtenspeicher Geänderter Ordner (keine Benachrichtigung an übergeordneten Ordner)  <br/> |
|Erstellen einer Nachricht  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher  <br/> |
|Löschen einer Nachricht, was zu einer Änderung in der **PR_CONTENT_COUNT** -Eigenschaft des übergeordneten Ordners führt  <br/> | _fnevObjectDeleted_ <br/> |Gelöschte Nachricht des Nachrichtenspeichers  <br/> |
|Verschieben einer Nachricht von einem Ordner in einen anderen  <br/> | _fnevObjectMoved_ <br/> |Nachrichtenspeicher-verschobene Nachricht  <br/> |
|Kopieren einer Nachricht von einem Ordner in einen anderen  <br/> | _fnevObjectCopied_ <br/> |Nachrichtenspeicher kopierte Nachricht (keine _fnevObjectCreated_ -Benachrichtigung für neue Kopie der Nachricht)  <br/> |
|Speichern einer Nachricht, was zu einer Änderung in der **PR_CONTENT_COUNT** -Eigenschaft des übergeordneten Ordners führt  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher nur beim ersten Speichern  <br/> |
|Speichern einer Nachricht  <br/> | _fnevObjectModified_ <br/> |Nachrichtenspeicher nach der ersten Speicherung geänderter Nachricht (keine Benachrichtigung an übergeordneten Ordner)  <br/> |
|Abschließen eines Suchvorgangs  <br/> | _fnevSearchComplete_ <br/> |Nachrichtenspeicher-Suchordner  <br/> |
|Neue Nachricht  <br/> | _Uleventmaskfnevnewmail_ <br/> |Nachrichtenspeicher  <br/> |
   
> [!NOTE]
> Wenn Sie eine geänderte Objekt Benachrichtigung erhalten, denken Sie daran, dass der Array Teil der [OBJECT_NOTIFICATION](object_notification.md) -Struktur, auf den durch den _lpNotifications_ -Parameter **** im OnNotify-Aufruf verwiesen wird, möglicherweise den Wert NULL hat oder nicht. Nachrichtenspeicher Anbieter sind nicht zum Einfügen von Eigenschaftsinformationen in diesem Array und die meisten nicht erforderlich. Stellen Sie sicher **** , dass Ihre OnNotify-Methode den Fall behandeln kann, dass der _LPPROPTAGARRAY_ -Zeiger NULL ist. 
  
Aktualisieren Sie für die meisten, wenn nicht alle Objekt Benachrichtigungen, die Ansicht des betreffenden Ordners oder der betroffenen Ordner.
  

