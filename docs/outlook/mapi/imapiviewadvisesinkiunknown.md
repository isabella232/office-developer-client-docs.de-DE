---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b7486139818ede9bd7e4b66472317ab50b05ba4d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567375"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Empfängt Benachrichtigungen von Formularen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anzeigen von empfohlenen Senkenobjekten  <br/> |
|Implementiert von:  <br/> |Formularanzeigen  <br/> |
|Aufgerufen von:  <br/> |Formularobjekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Benachrichtigt die Formularanzeige, dass ein Formular geschlossen wird.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Benachrichtigt die Formularanzeige, dass eine neue oder eine vorhandene Nachricht in einem Formular geladen wurde.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Benachrichtigt die Formularanzeige über den Druckstatus eines Formulars.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Benachrichtigt die Formularanzeige, dass die aktuelle Nachricht an den MAPI-Spooler gesendet wurde.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Benachrichtigt die Formularanzeige, dass die aktuelle Nachricht in einem Formular gespeichert wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

