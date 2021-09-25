---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c7102f49f678ae32d8aa0788703004ba3bfabe74
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579915"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Formularservern den Empfang von Benachrichtigungen von Formularviewern. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formular rät Senkenobjekten  <br/> |
|Implementiert von:  <br/> |Formularserver  <br/> |
|Aufgerufen von:  <br/> |Formularanzeigen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Gibt an, dass im Status der Formularanzeige eine Änderung vorgenommen wurde.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Gibt an, ob das Formular die Nachrichtenklasse der nächsten anzuzeigenden Nachricht verarbeiten kann.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Formularserver verwenden ein Formular-Empfehlungs-Senkenobjekt, um **IMAPIFormAdviseSink** zu implementieren, anstatt es in das Formularobjekt einzuschmieren. Daher sollten Formularviewer einen fehlgeschlagenen Aufruf der [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) eines Formulars erwarten, um einen Zeiger auf diese Schnittstelle abzurufen. 
  
Formularserver rufen die [IMAPIViewContext::SetAdviseSink-Methode](imapiviewcontext-setadvisesink.md) eines Viewers auf, um sich für Benachrichtigungen zu registrieren. Ein Zeiger auf ihre **IMAPIFormAdviseSink-Implementierung** ist als Parameter enthalten. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

