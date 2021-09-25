---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6df344d6fc63bef9ee475437810e7dbdc290786d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625364"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt einen Mechanismus zum Synchronisieren von E-Mails bereit, anstatt die Transport-API zu verwenden. Diese Schnittstelle wird für ein Store-Objekt verfügbar gemacht. Mithilfe dieser Schnittstelle und [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)kann ein Transportanbieter bessere Status- und Fehlermeldungen bereitstellen als die, die im Dialogfeld "Senden/Empfangen" in Microsoft Outlook angezeigt werden.
  
Der Posteingang befindet sich weiterhin im Standardspeicher. Outlook verwenden weiterhin die Transport-APIs zum Senden von E-Mails, da sich die ausgehende Nachricht nicht im externen Speicher befinden kann.
  
|||
|:-----|:-----|
|Verf�gbar gemacht von:  <br/> |Store- und Transportanbieter  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Store- und Transportanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implementiert von Nachrichtenspeicheranbietern. Diese Methode wird von Outlook 2010 und Outlook 2013 aufgerufen, um die Synchronisierung zu starten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[MAPI-Schnittstellen](mapi-interfaces.md)

