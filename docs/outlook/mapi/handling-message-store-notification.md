---
title: Behandeln von Nachrichtenspeicherbenachrichtigungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e8a312db93f3bd8e27c8c1e993bb7d3381f9159e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564379"
---
# <a name="handling-message-store-notification"></a>Behandeln von Nachrichtenspeicherbenachrichtigungen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um sich für Nachrichtenspeicherbenachrichtigungen zu registrieren, rufen Sie entweder die [IMAPISession::Advise-](imapisession-advise.md) oder [die IMsgStore::Advise-Methode](imsgstore-advise.md) auf, und geben Sie einen Nachrichtenspeicher-, Ordner- oder Nachrichteneintragsbezeichner im Inhalt des  _lpEntryID-Parameters_ an. Nachrichtenspeicheranbieter unterstützen Sowohl Objekt- als auch Tabellenbenachrichtigungen. Ob Sie sich bei bestimmten Nachrichtenspeicherobjekten, mit der Ordnerhierarchie und inhaltstabellen, die diese Objekte beschreiben, oder mit beiden Objekten und Tabellen registrieren, hängt von den erwarteten Benachrichtigungen, den Aufrufen zum Ausführen von Vorgängen und davon ab, wie der Nachrichtenspeicheranbieter Benachrichtigungen unterstützt. 
  
Da die MAPI flexibilitätsfähig ist, wie Anbieter Benachrichtigungen unterstützen, sollten Sie beachten, dass Sie nicht immer den gleichen Benachrichtigungstyp als Reaktion auf ein bestimmtes Ereignis von allen Nachrichtenspeicheranbietern erhalten. Einige Nachrichtenspeicheranbieter unterstützen keine Benachrichtigungen. Um festzustellen, ob der von Ihnen verwendete Nachrichtenspeicher Benachrichtigungen unterstützt, suchen Sie in der **eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) nach dem STORE_NOTIFY_OK Bit.
  
An einem Ende des Spektrums von Nachrichtenspeicheranbietern, die Benachrichtigungen unterstützen, sind die Anbieter, die "umfangreiche" Benachrichtigungen generieren. diese Anbieter senden beschreibende Benachrichtigungen für alle registrierten Empfehlungsquellen. Am anderen Ende befinden sich die Nachrichtenspeicheranbieter, die eingeschränkte Benachrichtigungen unterstützen. diese Anbieter senden allgemeine Benachrichtigungen für eine eingeschränkte Anzahl von Empfehlungsquellen. 
  
Wenn Sie z. B. eine Nachricht in einen Ordner kopieren, in dem Sie registriert sind, um Benachrichtigungen über kopierte Objekte und Objekte zu empfangen, erhalten Sie möglicherweise die Benachrichtigung über das kopierte Objekt oder nicht. Ob Sie es erhalten, hängt von folgendem ab:
  
- Die Methode, die Sie aufgerufen haben, um die Kopie auszuführen. Dies kann [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)oder [IMAPIProp::CopyProps](imapiprop-copyprops.md)sein.
    
- Implementierung der Kopiermethode durch den Nachrichtenspeicheranbieter.
    
- Gibt an, ob der Nachrichtenspeicheranbieter Benachrichtigungen über kopierte Objekte in Ordnern unterstützt.
    
Da es keine strengen Richtlinien gibt, die beschreiben, wie Ereignisbenachrichtigungen für Nachrichtenspeicheranbieter implementiert werden, können Clients kein konsistentes Verhalten erwarten. MapI gibt Empfehlungen dazu, wie Nachrichtenspeicheranbieter Ereignisbenachrichtigungen implementieren, und in der folgenden Tabelle werden diese Empfehlungen beschrieben. Lesen Sie die Tabelle wie folgt: Nachdem Sie den Vorgang in der ersten Spalte ausgeführt haben, erhalten Sie eine Benachrichtigung über den in der zweiten Spalte aufgeführten Typ, wenn Sie sich für diesen Typ mit dem in der dritten Spalte aufgeführten Objekt registriert haben. Nachdem Sie z. B. einen Ordner erstellt haben, erhalten Sie eine  _fnevObjectCreated-Benachrichtigung_ nur, wenn Sie sich für  _fnevObjectCreated-Benachrichtigungen_ beim Nachrichtenspeicher registriert haben. 
  
|**Vorgang**|**Ereignistyp**|**Empfehlungsquelle**|
|:-----|:-----|:-----|
|Erstellen eines Ordners  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher  <br/> |
|Löschen eines Ordners  <br/> | _fnevObjectDeleted_ <br/> |Ordner "Nachrichtenspeicher gelöscht"  <br/> |
|Verschieben eines Ordners von einem Ordner in einen anderen  <br/> | _fnevObjectMoved_ <br/> |Ordner "Nachrichtenspeicher verschoben"  <br/> |
|Kopieren eines Ordners von einem Ordner in einen anderen  <br/> | _fnevObjectCopied_ <br/> |Nachrichtenspeicher und kopierter Ordner (keine  _fnevObjectCreated-Benachrichtigung_ für die neue Kopie des Ordners gesendet)  <br/> |
|Änderung in einer berechneten Ordnereigenschaft (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Ordner "Nachrichtenspeicher geändert" (keine Benachrichtigung an übergeordneten Ordner)  <br/> |
|Erstellen einer Nachricht  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher  <br/> |
|Löschen einer Nachricht, wodurch eine Änderung in der **eigenschaft PR_CONTENT_COUNT** des übergeordneten Ordners verursacht wird  <br/> | _fnevObjectDeleted_ <br/> |Nachricht gespeichert Gelöschte Nachricht  <br/> |
|Verschieben einer Nachricht von einem Ordner in einen anderen  <br/> | _fnevObjectMoved_ <br/> |Nachrichtenspeicher Nachricht verschoben  <br/> |
|Kopieren einer Nachricht aus einem Ordner in einen anderen  <br/> | _fnevObjectCopied_ <br/> |Nachricht gespeichert Nachricht kopiert (keine  _fnevObjectCreated-Benachrichtigung_ für neue Kopie der Nachricht)  <br/> |
|Speichern einer Nachricht, wodurch eine Änderung in der **eigenschaft PR_CONTENT_COUNT** des übergeordneten Ordners verursacht wird  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher beim ersten Speichern nur  <br/> |
|Speichern einer Nachricht  <br/> | _fnevObjectModified_ <br/> |Nachrichtenspeicher bei Speichern nach dem ersten Speichern geänderter Nachricht (keine Benachrichtigung an übergeordneten Ordner)  <br/> |
|Abschließen eines Suchvorgangs  <br/> | _fnevSearchComplete_ <br/> |Suchordner für Nachrichtenspeicher  <br/> |
|Neue Nachricht  <br/> | _fnevNewMail_ <br/> |Nachrichtenspeicher  <br/> |
   
> [!NOTE]
> Wenn Sie eine Objektänderungsbenachrichtigung erhalten, denken Sie daran, dass das Eigenschaftstagarray der [OBJECT_NOTIFICATION](object_notification.md) Struktur, auf die der  _parameter lpNotifications_ im **OnNotify-Aufruf** verweist, null sein kann oder nicht. Nachrichtenspeicheranbieter müssen keine Eigenschafteninformationen in dieses Array einfügen, die meisten nicht. Stellen Sie sicher, dass die **OnNotify-Methode** den Fall verarbeiten kann, in dem der  _lpPropTagArray-Zeiger_ NULL ist. 
  
Aktualisieren Sie für die meisten, wenn nicht alle Objektbenachrichtigungen, die Ansicht des betroffenen Ordners oder der betroffenen Ordner.
  

