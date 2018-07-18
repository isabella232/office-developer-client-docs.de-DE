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
ms.openlocfilehash: bce70d891bc33dcddb94fc05992c09991c6cdc63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792441"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Betrifft**: Outlook 
  
Übergibt Speicheranbieter als Feld auf der Struktur MAPISIB während eines Anrufs auf [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md). Der Anbieter verwendet diese Schnittstelle ihr Feedback an Microsoft Outlook über den Status der Synchronisierung zu übermitteln.
  
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
|[Progress](imapisyncprogresscallback-progress.md) <br/> |Speicheranbieter ruft in regelmäßigen Abständen diese Funktion zum Aktualisieren des Status im Dialogfeld senden/empfangen.  <br/> |
|[Fehler](imapisyncprogresscallback-error.md) <br/> |Wenn während der Synchronisierung Fehler auftreten, ruft der Anbieter diese Funktion, um Details bereitstellen, die im Dialogfeld Senden/Empfangen angezeigt werden.  <br/> |
|[Fertig](imapisyncprogresscallback-done.md) <br/> |Speicheranbieter ruft diese Funktion, um Outlook zu informieren, dass die Synchronisierung abgeschlossen ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISync : IUnknown](imapisynciunknown.md)


[MAPI-Schnittstellen](mapi-interfaces.md)

