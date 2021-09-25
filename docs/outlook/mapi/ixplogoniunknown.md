---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3e508bd1515d629c8f53c0742fd55fdc0c2c5f67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592193"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gewährt dem MAPI-Spooler Zugriff auf einen Transportanbieter. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Transport von Anmeldeobjekten  <br/> |
|Implementiert von:  <br/> |Transportanbieter  <br/> |
|Aufgerufen von:  <br/> |Der MAPI-Spooler  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IXPLogon  <br/> |
|Zeigertyp:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Gibt die Empfängertypen zurück, die der Transportanbieter verarbeitet.  <br/> |
|**RegisterOptions** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Signalisiert das Auftreten eines Ereignisses, über das der Transportanbieter eine Benachrichtigung angefordert hat.  <br/> |
|[Im leerlauf](ixplogon-idle.md) <br/> |Gibt an, dass das System im Leerlauf ist, sodass der Transportanbieter Vorgänge mit niedriger Priorität ausführen kann.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Initiiert den Abmeldevorgang.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Gibt an, dass der MAPI-Spooler über eine Nachricht verfügt, die der Transportanbieter übermitteln soll.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informiert den Transportanbieter, dass der MAPI-Spooler die Verarbeitung für eine ausgehende Nachricht abgeschlossen hat.  <br/> |
|[Umfrage](ixplogon-poll.md) <br/> |Gibt an, ob der Transportanbieter eine oder mehrere eingehende Nachrichten empfangen hat.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Initiiert die Übertragung einer eingehenden Nachricht vom Transportanbieter an den MAPI-Spooler.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Öffnet das Statusobjekt des Transportanbieters.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Überprüft den externen Status des Transportanbieters.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Fordert an, dass der Transportanbieter alle ausstehenden eingehenden oder ausgehenden Nachrichten sofort übermittelt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

