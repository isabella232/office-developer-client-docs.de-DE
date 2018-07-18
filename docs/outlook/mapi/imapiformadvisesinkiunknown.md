---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fd2575d401aa8a39d6f3b2cd08377b587b430ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792140"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Betrifft**: Outlook 
  
Formular von Servern zum Formular Viewer Benachrichtigungen erhalten können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formular advise-Empfängerobjekten  <br/> |
|Implementiert von:  <br/> |Formular-Servern  <br/> |
|Aufgerufen von:  <br/> |Formular-Viewer  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Gibt an, dass eine Änderung in den Status des Formular-Viewers aufgetreten ist.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Gibt an, ob das Formular die Nachrichtenklasse für die nächste anzuzeigende Meldung verarbeiten kann.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Formular Servern mit einem Formular advise-Empfängerobjekt **IMAPIFormAdviseSink** implementieren, anstatt mit ihren Form-Objekt. Aus diesem Grund sollten Formular Viewer erwarten, einen Fehler beim Aufruf von [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) -Methode des Formulars einen Zeiger auf diese Schnittstelle abrufen. 
  
Formular Servern rufen Sie einen Viewer [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode für Benachrichtigungen registriert. Ein Zeiger auf ihre Implementierung **IMAPIFormAdviseSink** ist als Parameter enthalten. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

