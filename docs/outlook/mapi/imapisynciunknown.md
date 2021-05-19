---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405592"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt einen Mechanismus zum Synchronisieren von E-Mails anstelle der Transport-API bereit. Diese Schnittstelle wird für ein Store-Objekt verfügbar gemacht. Mit dieser Schnittstelle und [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)kann ein Transportanbieter bessere Fortschritts- und Fehlermeldungen bereitstellen als diejenigen, die im Dialogfeld Senden/Empfangen in Microsoft Outlook angezeigt werden.
  
Der Posteingang befindet sich weiterhin im Standardspeicher. Outlook verwendet weiterhin die Transport-APIs zum Senden von E-Mails, da die ausgehende Nachricht nicht im externen Speicher gespeichert werden kann.
  
|||
|:-----|:-----|
|Verf�gbar gemacht von:  <br/> |Speicher- und Transportanbieter  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Store- und Transportanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implementiert von Nachrichtenspeicheranbietern. Diese Methode wird von Outlook 2010 und Outlook 2013 aufgerufen, um die Synchronisierung zu starten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[MAPI-Schnittstellen](mapi-interfaces.md)

