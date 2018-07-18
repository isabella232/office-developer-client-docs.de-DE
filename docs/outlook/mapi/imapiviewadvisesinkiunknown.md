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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792483"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Betrifft**: Outlook 
  
Er empfängt Benachrichtigungen von Formularen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Empfängerobjekten advise-Ansicht  <br/> |
|Implementiert von:  <br/> |Formular-Viewer  <br/> |
|Aufgerufen von:  <br/> |Formular-Objekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Benachrichtigt dem Formular-Viewer, dass ein Formular geschlossen wird.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Benachrichtigt dem Formular-Viewer, dass eine neue oder eine vorhandene Nachricht in einem Formular geladen wurde.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Benachrichtigt den Formular-Viewer des Status eines Formulars drucken.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Benachrichtigt dem Formular-Viewer, dass die aktuelle Nachricht zu MAPI-Warteschlange gesendet wurde.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Benachrichtigt den Formular-Viewer, den die aktuelle Nachricht in einem Formular gespeichert wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

