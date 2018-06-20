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
ms.openlocfilehash: e8267b254648870cea4e16b4dea0e9c92e316fb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792881"
---
# <a name="itnef--iunknown"></a>ITnef: IUnknown

  
  
**Betrifft**: Outlook 
  
Bietet Methoden zum Kapseln von MAPI-Eigenschaften, die nicht von einem messaging-System in binären Streams unterstützt werden, die Nachrichten zugeordnet werden kann. Das Format für diese Kapselung ist der Transport-Neutral Encapsulation Format (TNEF). Die Ziel-Transport-Anbieter oder MAPI-basierter Client-Anwendung können Sie dann auf Empfangen einer Nachricht, die TNEF-Anlage enthält, die Eigenschaften aus der Anlage wiederherstellen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF.h  <br/> |
|Verf�gbar gemacht von:  <br/> |TNEF-Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Transport-Provider, Anbieter Nachricht und gateways  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_ITNEF  <br/> |
|Zeigertyp:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Ermöglicht die aufrufende Dienstanbieter oder Gateway Eigenschaften, die Kapselung einer Nachricht oder eine Anlage hinzuzufügen.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrahiert die Eigenschaften von TNEF-Kapselung.  <br/> |
|[Finish](itnef-finish.md) <br/> |Beendet Verarbeitung für alle TNEF-Vorgänge, die sich in der Warteschlange und wartet.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Öffnet eine Stream-Schnittstelle für den Text der Fehlermeldung der gekapselte.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage ohne Ändern der ursprünglichen Nachricht oder Anlage fest.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Codiert eine Ansicht für die Empfänger einer Nachricht-Tabelle in der TNEF-Datenstrom für die Nachricht an.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Verarbeitet aus einer Nachricht an eine einzelne Komponenten zu einem Zeitpunkt in einem TNEF-Stream.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

