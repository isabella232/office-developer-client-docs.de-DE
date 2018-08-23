---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cffa3024b8533f07f8f76fa5bbac219e23d61bdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589504"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Nachrichten bearbeitet und wird durch die Viewer Formularcode (normalerweise eine Clientanwendung), die auf eine solche Bearbeitung reagiert implementiert.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verfügbar gemacht von:  <br/> |Nachricht Websiteobjekten  <br/> |
|Implementiert von:  <br/> |Formular-Viewer  <br/> |
|Aufgerufen von:  <br/> |Formular-Objekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIMessageSite  <br/> |
|Zeigertyp:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Gibt die MAPI-Sitzung, in der die aktuelle Nachricht erstellt oder geöffnet wurde.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Gibt den Nachrichtenspeicher, der die aktuelle Nachricht enthält zurück, wenn eine solche ein Speicher vorhanden ist.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Der Ordner, in dem die aktuelle Nachricht geöffnet oder erstellt wurde, zurückgegeben, wenn solche ein Ordner vorhanden ist.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Gibt die aktuelle Nachricht zurück.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Gibt eine Formular-Manager-Schnittstelle, die ein Formular Server verwenden kann, um ein anderes Formular Server zu öffnen.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Erstellt eine neue Nachricht an.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Kopiert die aktuelle Nachricht in einen Ordner.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Verschiebt die aktuelle Nachricht in einen Ordner.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Löscht die aktuelle Nachricht.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Anforderungen, die die aktuelle Nachricht gespeichert werden soll.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Fordert, dass die aktuelle Nachricht für die Übermittlung in die Warteschlange gestellt werden.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Gibt Informationen aus einem Objekt "Message" Website zur Nachricht der Website Funktionen für die aktuelle Nachricht zurück.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftreten, um das Objekt "Message" Website enthält.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

