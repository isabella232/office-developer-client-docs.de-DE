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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 75ef8d6f2134e0269745f92dab1f790228692853
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792238"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Betrifft**: Outlook 
  
Nachrichten bearbeitet und wird durch die Viewer Formularcode (normalerweise eine Clientanwendung), die auf eine solche Bearbeitung reagiert implementiert.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachricht Websiteobjekten  <br/> |
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

