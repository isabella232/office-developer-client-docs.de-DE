---
title: Behandeln von Store-Benachrichtigung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 898f8b6ff3d0b0dd42a670596b54171f18b4a5e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791810"
---
# <a name="handling-message-store-notification"></a>Behandeln von Store-Benachrichtigung
  
**Betrifft**: Outlook 
  
Um Benachrichtigungen über Textnachrichten Store zu registrieren, rufen Sie die [IMAPISession::Advise](imapisession-advise.md) oder [IMsgStore::Advise](imsgstore-advise.md) -Methode, und geben Sie einen Nachrichtenspeicher, Ordner oder Eintrags-ID der Nachricht in den Inhalt des Parameters _LpEntryID_ . Nachricht Anbieter unterstützen Objekt und Tabelle. Ob Sie registrieren mit bestimmten Nachricht Store-Objekten, die Ordner Hierarchie und der Inhalt der Tabellen, die diese Objekte beschreiben oder beides Objekte und Tabellen hängt von der Benachrichtigungen angezeigt wird, die Anrufe Sie Operationen ausführen, stellen Sie erwarten und wie der Nachricht Speicheranbieter unterstützt die Benachrichtigung. 
  
Da MAPI Flexibilität bei der Unterstützung von Anbietern wie Benachrichtigungen, beachten Sie, dass Sie nicht immer den gleichen Typ der Benachrichtigung als Antwort auf ein bestimmtes Ereignis alle Nachricht-Anbieter empfängt. Einige Anbieter Nachricht unterstützen überhaupt keine Benachrichtigungen. Um festzustellen, ob der Nachrichtenspeicher verwendeten Benachrichtigung, suchen Sie nach der STORE_NOTIFY_OK Bit in der Eigenschaft **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) unterstützt.
  
An einem Ende des Spektrums des Nachrichtenspeichers sind Anbieter, die Benachrichtigung zu unterstützen die Anbieter, die "rich" Benachrichtigungen generieren. Diese Anbieter senden beschreibende Benachrichtigungen für alle registrierten advise-Quellen. An das andere Ende sind die Nachricht Speicheranbieter, beschränkte Benachrichtigungen zu unterstützen. Diese Anbieter senden allgemeine Benachrichtigungen für eine eingeschränkte Anzahl von Advise-Quellen. 
  
Beispielsweise kopieren eine Nachricht in einen Ordner mit dem Sie registriert haben, um empfangen beide-Objekt kopiert und Objekt verschoben, Benachrichtigungen oder anzeigen, kann möglicherweise nicht die Benachrichtigung-Objekt kopiert. Unabhängig davon, ob Sie erhalten hängt:
  
- Die Methode, die Sie aufgerufen, um die Kopie auszuführen. Dies kann [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)oder [IMAPIProp::CopyProps](imapiprop-copyprops.md)sein.
    
- Wie die Nachricht speichern Anbieter implementiert die Copy-Methode.
    
- Unabhängig davon, ob der Nachricht Speicheranbieter-Objekt kopiert Benachrichtigungen für Ordner unterstützt.
    
Da vorhanden, dass keine strengen Richtlinien, die zum Implementieren der Benachrichtigung für Nachricht beschreiben Anbieter speichern sind, können keine Clients durchgängigen erwarten. MAPI legt Empfehlungen vor, um wie Nachrichtenspeicher Anbieter implementieren Benachrichtigung und die in der folgenden Tabelle Konturen diesen Empfehlungen. Lesen die Tabelle wie folgt: nach dem Ausführen dieses Vorgangs in der ersten Spalte erwarten eine Benachrichtigung über den Typ in der zweiten Spalte aufgeführt werden, wenn Sie für diesen Typ, mit dem Objekt in der dritten Spalte aufgeführt registriert haben. Beispielsweise nachdem Sie einen Ordner erstellt haben, erhalten Sie eine _FnevObjectCreated_ Benachrichtigung nur, wenn Sie für _FnevObjectCreated_ Benachrichtigungen, mit dem Nachrichtenspeicher registriert haben. 
  
|**Vorgang**|**Ereignistyp**|**Advise-Quelle**|
|:-----|:-----|:-----|
|Erstellen eines Ordners  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher  <br/> |
|Löschen eines Ordners  <br/> | _fnevObjectDeleted_ <br/> |Nachrichtenspeicher Ordner gelöscht  <br/> |
|Verschieben Sie einen Ordner aus einem Ordner in einen anderen  <br/> | _fnevObjectMoved_ <br/> |Nachrichtenspeicher verschobene Ordner  <br/> |
|Kopieren eines Ordners aus einem Ordner in einen anderen  <br/> | _fnevObjectCopied_ <br/> |Nachricht speichern und kopiert Ordner (keine _FnevObjectCreated_ Benachrichtigung, die für die neue Kopie des Ordners)  <br/> |
|Ändern Sie in einem berechnete-Ordnereigenschaft (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Nachrichtenspeicher Changed-Ordner (keine Benachrichtigung an den übergeordneten Ordner)  <br/> |
|Erstellen Sie eine Nachricht  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher  <br/> |
|Löschen einer Nachricht, verursacht eine Änderung in der übergeordneten Ordners **PR_CONTENT_COUNT** -Eigenschaft  <br/> | _fnevObjectDeleted_ <br/> |Nachrichtenspeicher Deleted Nachricht  <br/> |
|Verschieben Sie eine Nachricht von einem Ordner in einen anderen  <br/> | _fnevObjectMoved_ <br/> |Nachrichtenspeicher verschobene Nachricht  <br/> |
|Kopieren Sie eine Nachricht von einem Ordner in einen anderen  <br/> | _fnevObjectCopied_ <br/> |Nachrichtenspeicher kopierte Nachricht (keine _FnevObjectCreated_ Benachrichtigung für die neue Kopie der Nachricht)  <br/> |
|Speichern einer Nachricht, verursacht eine Änderung in der übergeordneten Ordners **PR_CONTENT_COUNT** -Eigenschaft  <br/> | _fnevObjectCreated_ <br/> |Nachrichtenspeicher bei der ersten nur speichern  <br/> |
|Speichern einer Nachricht  <br/> | _fnevObjectModified_ <br/> |Nachrichtenspeicher auf speichert nach dem ersten Speichern Changed-Nachricht (keine Benachrichtigung an den übergeordneten Ordner)  <br/> |
|Führen Sie einen Suchvorgang  <br/> | _fnevSearchComplete_ <br/> |Nachrichtenspeicher Suchordner  <br/> |
|Neue Nachricht  <br/> | _fnevNewMail_ <br/> |Nachrichtenspeicher  <br/> |
   
> [!NOTE]
> Wenn Sie eine Benachrichtigung geänderten Objekt erhalten, denken Sie daran, dass der Eigenschaft Tag Array-Teil der [OBJECT_NOTIFICATION](object_notification.md) Struktur auf die _LpNotifications_ -Parameter im Aufruf **OnNotify** zeigt möglicherweise oder darf nicht NULL sein. Nachricht Anbieter sind nicht zum Einfügen von Informationen in diesem Array und am häufigsten nicht erforderlich. Stellen Sie sicher, dass Ihre **OnNotify** -Methode die Groß-/Kleinschreibung verarbeiten kann, auf dem der _LpPropTagArray_ Zeiger NULL ist. 
  
Bei den meisten wenn nicht alle Benachrichtigungen-Objekts, aktualisieren Sie die Ansicht der betreffenden Ordner oder Ordner.
  

