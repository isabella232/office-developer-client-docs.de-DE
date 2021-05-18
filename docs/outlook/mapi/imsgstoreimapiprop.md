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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422327"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf Nachrichtenspeicherinformationen sowie auf Nachrichten und Ordner.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Message store-Objekt  <br/> |
|Implementiert von:  <br/> |Anbieter von Nachrichtenspeichern  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen, mapi-Spooler und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMsgStore  <br/> |
|Zeigertyp:  <br/> |LPMDB  <br/> |
|Transaktionsmodell:  <br/> |Nichttransaktioniert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Raten](imsgstore-advise.md) <br/> |Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf den Nachrichtenspeicher auswirken.  <br/> |
|[Unadvise](imsgstore-unadvise.md) <br/> |Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMsgStore::Advise-Methode eingerichtet** wurden.  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf denselben Eintrag in einem Nachrichtenspeicher verweisen.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Öffnet einen Ordner oder eine Nachricht und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Richtet einen Ordner als Ziel für eingehende Nachrichten einer bestimmten Nachrichtenklasse ein.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als Standard-Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Bietet Zugriff auf die Tabelle "Empfangsordner", eine Tabelle mit Informationen zu allen Empfangsordnern für den Nachrichtenspeicher.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Aktiviert die geordnete Abmeldung des Nachrichtenspeichers.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Bietet Zugriff auf die Tabelle für ausgehende Warteschlangen, eine Tabelle mit Informationen zu allen Nachrichten in der ausgehenden Warteschlange des Nachrichtenspeichers.  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Sperrt oder entsperrt eine Nachricht.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Ermöglicht dem Nachrichtenspeicheranbieter die Verarbeitung einer gesendeten Nachricht.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat.  <br/> |
   
|**Erforderliche Eigenschaften**|**Zugriffsebene**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
Die folgenden Eigenschaften sind für Zwischenperson Message (IPM)-Nachrichtenspeicher:
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)

