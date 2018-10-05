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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392060"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formular von Servern zum Formular Viewer Benachrichtigungen erhalten können. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapiform.h  <br/> |
|Verfügbar gemacht von:  <br/> |Formular advise-Empfängerobjekten  <br/> |
|Implementiert von:  <br/> |Formular-Servern  <br/> |
|Aufgerufen von:  <br/> |Formular-Viewer  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Gibt an, dass eine Änderung in den Status des Formular-Viewers aufgetreten ist.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Gibt an, ob das Formular die Nachrichtenklasse für die nächste anzuzeigende Meldung verarbeiten kann.  <br/> |
   
## <a name="remarks"></a>Hinweise

Formular Servern mit einem Formular advise-Empfängerobjekt **IMAPIFormAdviseSink** implementieren, anstatt mit ihren Form-Objekt. Aus diesem Grund sollten Formular Viewer erwarten, einen Fehler beim Aufruf von [QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode des Formulars einen Zeiger auf diese Schnittstelle abrufen. 
  
Formular Servern rufen Sie einen Viewer [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode für Benachrichtigungen registriert. Ein Zeiger auf ihre Implementierung **IMAPIFormAdviseSink** ist als Parameter enthalten. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

