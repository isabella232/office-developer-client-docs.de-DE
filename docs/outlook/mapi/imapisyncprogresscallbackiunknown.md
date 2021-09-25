---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 502f43eb5caecbc9285036c5ab7eb14cafded65b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575778"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Übergibt den Speicheranbieter als Feld in der MAPISIB-Struktur während eines Aufrufs von [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md). Der Store-Anbieter verwendet diese Schnittstelle, um Microsoft Outlook Feedback zum Status der Synchronisierung zu geben.
  
|||
|:-----|:-----|
|Headerdatei  <br/> ||
|Verf�gbar gemacht von:  <br/> |Outlook  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Store Anbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |Der Store-Anbieter ruft diese Funktion in regelmäßigen Abständen auf, um den Status im Dialogfeld "Senden/Empfangen" zu aktualisieren.  <br/> |
|[Error](imapisyncprogresscallback-error.md) <br/> |Wenn während der Synchronisierung Fehler auftreten, ruft der Speicheranbieter diese Funktion auf, um Details bereitzustellen, die im Dialogfeld "Senden/Empfangen" angezeigt werden.  <br/> |
|[Done](imapisyncprogresscallback-done.md) <br/> |Der Store-Anbieter ruft diese Funktion auf, um Outlook darüber zu informieren, dass die Synchronisierung abgeschlossen wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISync : IUnknown](imapisynciunknown.md)


[MAPI-Schnittstellen](mapi-interfaces.md)

