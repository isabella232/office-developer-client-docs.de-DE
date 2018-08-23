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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 33d811af0fc9e06902750075ba39bfb6ca88903f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593711"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Übergibt Speicheranbieter als Feld auf der Struktur MAPISIB während eines Anrufs auf [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md). Der Anbieter verwendet diese Schnittstelle ihr Feedback an Microsoft Outlook über den Status der Synchronisierung zu übermitteln.
  
|||
|:-----|:-----|
|Headerdatei  <br/> ||
|Verfügbar gemacht von:  <br/> |Outlook  <br/> |
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

