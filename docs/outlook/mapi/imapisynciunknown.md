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
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589084"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bietet einen Mechanismus zum Synchronisieren von e-Mail statt der Transport-API. Diese Schnittstelle wird auf ein Store-Objekt verfügbar gemacht. Mithilfe dieser Schnittstelle und [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), ein Transportdienstes bieten eine bessere Bearbeitung und Fehlermeldungen als die, die im Dialogfeld senden/empfangen in Microsoft Outlook angezeigt werden.
  
Im Ordner Postausgang ist noch in der Standard-Informationsspeichers. Outlook wird weiterhin die Transport-APIs verwenden, um e-Mail-Nachrichten senden, da die ausgehende Nachricht im externen Speicher ist.
  
|||
|:-----|:-----|
|Verfügbar gemacht von:  <br/> |Anbieter für Speicher und transport  <br/> |
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

