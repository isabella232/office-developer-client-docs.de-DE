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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fb7a8ea39d6e7b1d7df1560658ceb67a79d39d92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792430"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Betrifft**: Outlook 
  
Bietet einen Mechanismus zum Synchronisieren von e-Mail statt der Transport-API. Diese Schnittstelle wird auf ein Store-Objekt verfügbar gemacht. Mithilfe dieser Schnittstelle und [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), ein Transportdienstes bieten eine bessere Bearbeitung und Fehlermeldungen als die, die im Dialogfeld senden/empfangen in Microsoft Outlook angezeigt werden.
  
Im Ordner Postausgang ist noch in der Standard-Informationsspeichers. Outlook wird weiterhin die Transport-APIs verwenden, um e-Mail-Nachrichten senden, da die ausgehende Nachricht im externen Speicher ist.
  
|||
|:-----|:-----|
|Verf�gbar gemacht von:  <br/> |Anbieter für Speicher und transport  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Anbieter für Speicher und Transport  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Nachricht Zeichenfolgeneigenschaften implementiert. Diese Methode wird von Outlook 2010 und Outlook 2013, um die Synchronisierung starten aufgerufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[MAPI-Schnittstellen](mapi-interfaces.md)

