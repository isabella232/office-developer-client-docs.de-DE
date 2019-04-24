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
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286604"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Formular Servern das Empfangen von Benachrichtigungen von Formular Viewern. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Form Advise Sink-Objekte  <br/> |
|Implementiert von:  <br/> |Formularserver  <br/> |
|Aufgerufen von:  <br/> |Formular Betrachter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Gibt an, dass eine Änderung im Status des Formular-Viewers aufgetreten ist.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Gibt an, ob das Formular die Nachrichtenklasse der nächsten anzuzeigende Nachricht behandeln kann.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Formularserver verwenden ein Advise-Senke-Objekt, um **IMAPIFormAdviseSink** zu implementieren, anstatt Sie mit Ihrem Form-Objekt einzubinden. Daher sollten Formular Betrachter einen fehlgeschlagenen Aufruf der [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode eines Formulars erwarten, um einen Zeiger auf diese Schnittstelle abzurufen. 
  
Formularserver rufen die [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode eines Viewers auf, um sich für Benachrichtigungen zu registrieren. Ein Zeiger auf Ihre **IMAPIFormAdviseSink** -Implementierung ist als Parameter enthalten. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

