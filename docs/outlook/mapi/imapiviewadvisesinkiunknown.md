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
ms.openlocfilehash: 157703fc9702bb954b4a5c570fc3d5c045e181cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567188"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Er empfängt Benachrichtigungen von Formularen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verfügbar gemacht von:  <br/> |Empfängerobjekten advise-Ansicht  <br/> |
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

