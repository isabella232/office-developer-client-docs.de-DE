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
ms.openlocfilehash: 426333e6e2624adcd7cb6bc6dc4982b3d1ef1999
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792651"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore: IMAPIProp

  
  
**Betrifft**: Outlook 
  
Bietet Zugriff auf Informationen zu Märkten Nachricht und Nachrichten und Ordnern.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Objekt "Message" store  <br/> |
|Implementiert von:  <br/> |Nachricht-Anbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen, die MAPI-Warteschlange und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMsgStore  <br/> |
|Zeigertyp:  <br/> |LPMDB  <br/> |
|Transaktionsmodell:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Beraten](imsgstore-advise.md) <br/> |Um die Benachrichtigung der angegebenen Ereignisse, die Einfluss auf die Nachrichtenspeicher registriert.  <br/> |
|[Heben Sie diesen Vorgang](imsgstore-unadvise.md) <br/> |Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode **IMsgStore::Advise** eingerichtet.  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um festzustellen, ob sie auf dieselbe Rechtsgrundlage in einem Nachrichtenspeicher verweisen.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Öffnet einen Ordner oder eine Nachricht, und gibt einen Schnittstellenzeiger für den weiteren Zugriff.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Stellt einen Ordner als Ziel für eingehende Nachrichten von einer bestimmten Nachrichtenklasse her.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Ruft den Ordner, der als Ziel für eingehende Nachrichten von einer angegebenen Nachrichtenklasse oder als Standard Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Bietet Zugriff auf die empfangen Ordnertabelle eine Tabelle mit Informationen zu allen der Ordner für den Nachrichtenspeicher empfangen.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Ermöglicht das ordnungsgemäße Abmelden des Nachrichtenspeichers.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Bietet Zugriff auf ausgehende Warteschlangentabelle eine Tabelle mit Informationen über alle Nachrichten in der Nachrichtenspeicher ausgehenden Warteschlange.  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Sperrt oder entsperrt eine Nachricht.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Aktiviert den Nachricht-Speicher-Anbieter für die Verarbeitung für eine gesendete Nachricht.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat.  <br/> |
   
|**Erforderliche Eigenschaften**|**Zugriffsebene**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
Die folgenden Eigenschaften sind für Nachrichtenspeicher zwischen Personen Nachricht (IPM):
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)

