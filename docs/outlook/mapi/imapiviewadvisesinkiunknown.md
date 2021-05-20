---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429418"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Empfängt Benachrichtigungen von Formularen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anzeigen von Ratensenkenobjekten  <br/> |
|Implementiert von:  <br/> |Formularanzeigen  <br/> |
|Aufgerufen von:  <br/> |Formularobjekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Benachrichtigt die Formularanzeige, dass ein Formular geschlossen wird.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Benachrichtigt die Formularanzeige, dass eine neue oder eine vorhandene Nachricht in einem Formular geladen wurde.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Benachrichtigt die Formularanzeige über den Druckstatus eines Formulars.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Benachrichtigt die Formularanzeige, dass die aktuelle Nachricht an den MAPI-Spooler übermittelt wurde.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Benachrichtigt die Formularanzeige, dass die aktuelle Nachricht in einem Formular gespeichert wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

