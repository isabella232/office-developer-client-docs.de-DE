---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7cc27b5d5ce3b0bbfd2dd407248be60a6baa157b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575911"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bearbeitet Nachrichten und wird vom Formularanzeigecode (in der Regel eine Clientanwendung) implementiert, der auf diese Manipulation reagiert.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtenwebsiteobjekte  <br/> |
|Implementiert von:  <br/> |Formularanzeigen  <br/> |
|Aufgerufen von:  <br/> |Formularobjekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIMessageSite  <br/> |
|Zeigertyp:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Gibt die MAPI-Sitzung zurück, in der die aktuelle Nachricht erstellt oder geöffnet wurde.  <br/> |
|[Getstore](imapimessagesite-getstore.md) <br/> |Gibt den Nachrichtenspeicher zurück, der die aktuelle Nachricht enthält, wenn ein solcher Speicher vorhanden ist.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Gibt den Ordner zurück, in dem die aktuelle Nachricht erstellt oder geöffnet wurde, wenn ein solcher Ordner vorhanden ist.  <br/> |
|[Getmessage](imapimessagesite-getmessage.md) <br/> |Gibt die aktuelle Nachricht zurück.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Gibt eine Formular-Manager-Schnittstelle zurück, die ein Formularserver zum Öffnen eines anderen Formularservers verwenden kann.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Erstellt eine neue Nachricht.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Kopiert die aktuelle Nachricht in einen Ordner.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Verschiebt die aktuelle Nachricht in einen Ordner.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Löscht die aktuelle Nachricht.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Fordert an, dass die aktuelle Nachricht gespeichert wird.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Fordert an, dass die aktuelle Nachricht zur Zustellung in die Warteschlange gestellt wird.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Gibt Informationen von einem Nachrichtenwebsiteobjekt zu den Funktionen der Nachrichtenwebsite für die aktuelle Nachricht zurück.  <br/> |
|[Getlasterror](imapimessagesite-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Nachrichtenwebsiteobjekt aufgetreten ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

