---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315036"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Methoden zum Kapseln von MAPI-Eigenschaften bereit, die von einem Messagingsystem nicht in binäre Streams unterstützt werden, die an Nachrichten angefügt werden können. Das für diese Kapselung verwendete Format ist das Transport neutrale Encapsulation Format (TNEF). Der Ziel Transportanbieter oder die MAPI-basierte Clientanwendung kann dann beim Empfang einer Nachricht, die eine TNEF-Anlage enthält, die Eigenschaften aus der Anlage wiederherstellen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF. h  <br/> |
|Verf�gbar gemacht von:  <br/> |TNEF-Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_ITNEF  <br/> |
|Zeigertyp:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Ermöglicht dem aufrufenden Dienstanbieter oder Gateway das Hinzufügen von Eigenschaften zur Kapselung einer Nachricht oder Anlage.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrahiert die Eigenschaften aus einer TNEF-Kapselung.  <br/> |
|[Finish](itnef-finish.md) <br/> |Die Verarbeitung für alle in der Warteschlange befindlichen TNEF-Vorgänge wird abgeschlossen.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Öffnet eine Stream-Schnittstelle für den Text einer gekapselte Nachricht.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage fest, ohne die ursprüngliche Nachricht oder Anlage zu ändern.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Codiert eine Ansicht für die Empfängertabelle einer Nachricht im TNEF-Datenstrom für die Nachricht.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Verarbeitet einzelne Komponenten aus einer Nachricht nacheinander in einem TNEF-Stream.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

