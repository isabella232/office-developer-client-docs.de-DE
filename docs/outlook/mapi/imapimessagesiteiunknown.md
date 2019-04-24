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
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321350"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bearbeitet Nachrichten und wird vom Formularanzeige Code (in der Regel eine Clientanwendung) implementiert, der auf eine solche Manipulation reagiert.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtenwebsite Objekte  <br/> |
|Implementiert von:  <br/> |Formular Betrachter  <br/> |
|Aufgerufen von:  <br/> |Formularobjekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIMessageSite  <br/> |
|Zeigertyp:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetSession "](imapimessagesite-getsession.md) <br/> |Gibt die MAPI-Sitzung zurück, in der die aktuelle Nachricht erstellt oder geöffnet wurde.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Gibt den Nachrichtenspeicher zurück, der die aktuelle Nachricht enthält, wenn ein solcher Speicher vorhanden ist.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Gibt den Ordner zurück, in dem die aktuelle Nachricht erstellt oder geöffnet wurde, wenn ein solcher Ordner vorhanden ist.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Gibt die aktuelle Nachricht zurück.  <br/> |
|[GetFormmanager](imapimessagesite-getformmanager.md) <br/> |Gibt eine Formular-Manager-Schnittstelle zurück, die ein Formularserver zum Öffnen eines anderen Formular Servers verwenden kann.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Erstellt eine neue Nachricht.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Kopiert die aktuelle Nachricht in einen Ordner.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Verschiebt die aktuelle Nachricht in einen Ordner.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Löscht die aktuelle Nachricht.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Fordert, dass die aktuelle Nachricht gespeichert wird.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Fordert an, dass die aktuelle Nachricht für die Übermittlung in die Warteschlange gestellt wird.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Gibt Informationen aus einem Nachrichtenwebsite Objekt über die Funktionen der Nachrichtenwebsite für die aktuelle Nachricht zurück.  <br/> |
|[Getlasterroraufzurufen](imapimessagesite-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der für das Nachrichtenwebsite Objekt auftritt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

