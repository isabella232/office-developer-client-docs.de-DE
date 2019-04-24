---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348720"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf Nachrichtenspeicher Informationen und für Nachrichten und Ordner.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtenspeicherobjekt  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher Anbieter  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen, MAPI-Spooler und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMsgStore  <br/> |
|Zeigertyp:  <br/> |LPMDB  <br/> |
|Transaktionsmodell:  <br/> |Nicht durchgeführten  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Beraten](imsgstore-advise.md) <br/> |Registriert die Benachrichtigung über angegebene Ereignisse, die sich auf den Nachrichtenspeicher auswirken.  <br/> |
|[Unadvise](imsgstore-unadvise.md) <br/> |Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMsgStore:: Advise** -Methode eingerichtet wurden.  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf den gleichen Eintrag in einem Nachrichtenspeicher verweisen.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Öffnet einen Ordner oder eine Nachricht und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Richtet einen Ordner als Ziel für eingehende Nachrichten einer bestimmten Nachrichtenklasse ein.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als standardmäßiger Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Ermöglicht den Zugriff auf die Tabelle Receive Folder, eine Tabelle mit Informationen zu allen Empfangs Ordnern für den Nachrichtenspeicher.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Aktiviert die ordnungsgemäße Abmeldung des Nachrichtenspeichers.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Ermöglicht den Zugriff auf die Tabelle für ausgehende Warteschlangen, eine Tabelle mit Informationen zu allen Nachrichten in der ausgehenden Warteschlange des Nachrichtenspeichers.  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Sperrt oder entsperrt eine Nachricht.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Ermöglicht dem Nachrichtenspeicher Anbieter das Ausführen der Verarbeitung für eine gesendete Nachricht.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat.  <br/> |
   
|**Erforderliche Eigenschaften**|**Zugriffsebene**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_ENTRYID** ([Pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_RECORD_KEY** ([Pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MDB_PROVIDER** ([Pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
Die folgenden Eigenschaften sind für Nachrichtenspeicher zwischen Personen Nachrichten (IPM):
  
- **PR_IPM_OUTBOX_ENTRYID** ([Pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([Pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([Pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([Pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)

