---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341237"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Übergibt den Informationsspeicher Anbieter während eines Aufrufs an [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)als Feld der MAPISIB-Struktur. Der Informationsspeicher Anbieter verwendet diese Schnittstelle, um Microsoft Outlook Feedback zum Status der Synchronisierung bereitzustellen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> ||
|Verf�gbar gemacht von:  <br/> |Outlook  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Speicheranbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |Der Informationsspeicher Anbieter ruft diese Funktion in regelmäßigen Abständen auf, um den Status im Dialogfeld senden/empfangen zu aktualisieren.  <br/> |
|[Error](imapisyncprogresscallback-error.md) <br/> |Wenn während der Synchronisierung Fehler auftreten, ruft der Informationsspeicher Anbieter diese Funktion auf, um Details bereitzustellen, die im Dialogfeld senden/empfangen angezeigt werden.  <br/> |
|[Done](imapisyncprogresscallback-done.md) <br/> |Der Informationsspeicher Anbieter ruft diese Funktion auf, um Outlook zu benachrichtigen, dass die Synchronisierung abgeschlossen wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISync : IUnknown](imapisynciunknown.md)


[MAPI-Schnittstellen](mapi-interfaces.md)

