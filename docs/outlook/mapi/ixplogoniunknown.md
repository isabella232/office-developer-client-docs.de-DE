---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ecfbf33641c86d4f162c521466ca2bf0b79a61d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581405"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den MAPI-Warteschlange Zugriff auf einem Transportdienstes. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verfügbar gemacht von:  <br/> |Transport Logon-Objekten  <br/> |
|Implementiert von:  <br/> |Transportanbieter  <br/> |
|Aufgerufen von:  <br/> |Die MAPI-Warteschlange  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IXPLogon  <br/> |
|Zeigertyp:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Gibt die Typen von Empfängern, die der Adressbuchhierarchie behandelt.  <br/> |
|**RegisterOptions** <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Signalisiert das Auftreten eines Ereignisses zu den der Transportdienst Benachrichtigung angefordert.  <br/> |
|[Im Leerlauf](ixplogon-idle.md) <br/> |Gibt an, dass das System im Leerlauf, der Adressbuchhierarchie niedriger Priorität Operationen aktivieren.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Initiiert den Prozess abmelden.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Gibt an, dass die MAPI-Warteschlange eine Nachricht an der Adressbuchhierarchie übermittelt wurde.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Der Transportdienst informiert werden, dass die MAPI-Warteschlange die Verarbeitung für eine ausgehende Nachricht abgeschlossen.  <br/> |
|[Umfrage](ixplogon-poll.md) <br/> |Gibt an, ob der Adressbuchhierarchie mindestens eine eingehende Nachricht empfangen hat.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Initiiert die Übertragung von einer eingehenden Nachricht aus der Adressbuchhierarchie auf die MAPI-Warteschlange.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Öffnet die Adressbuchhierarchie Status-Objekt.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Externe Status der Adressbuchhierarchie überprüft.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Fordert, dass der Adressbuchhierarchie sofort alle ausstehende eingehende oder ausgehende Nachrichten übermitteln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

