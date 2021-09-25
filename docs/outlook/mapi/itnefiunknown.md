---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bbb1af4676586c1dc5df353c6410436cb3d995df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613758"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Methoden zum Kapseln von MAPI-Eigenschaften bereit, die von einem Messagingsystem nicht in binäre Datenströme unterstützt werden, die an Nachrichten angefügt werden können. Das für diese Kapselung verwendete Format ist das Transport-Neutral Kapselungsformat (Encapsulation Format, TNEF). Der Zieltransportanbieter oder die MAPI-basierte Clientanwendung kann dann beim Empfangen einer Nachricht, die eine TNEF-Anlage enthält, die Eigenschaften aus der Anlage wiederherstellen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Tnef.h  <br/> |
|Verf�gbar gemacht von:  <br/> |TNEF-Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Transportanbieter, Nachrichtenspeicheranbieter und Gateways  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_ITNEF  <br/> |
|Zeigertyp:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Ermöglicht dem aufrufenden Dienstanbieter oder Gateway das Hinzufügen von Eigenschaften zur Kapselung einer Nachricht oder Anlage.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrahiert die Eigenschaften aus einer TNEF-Kapselung.  <br/> |
|[Finish](itnef-finish.md) <br/> |Beendet die Verarbeitung für alle TNEF-Vorgänge, die in die Warteschlange eingereiht sind und warten.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Öffnet eine Datenstromschnittstelle für den Text einer gekapselten Nachricht.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage fest, ohne die ursprüngliche Nachricht oder Anlage zu ändern.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Codiert eine Ansicht für die Empfängertabelle einer Nachricht im TNEF-Datenstrom für die Nachricht.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Verarbeitet einzelne Komponenten aus einer Nachricht nacheinander in einem TNEF-Stream.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

