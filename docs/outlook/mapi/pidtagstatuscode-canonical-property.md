---
title: PidTagStatusCode (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418514"
---
# <a name="pidtagstatuscode-canonical-property"></a>PidTagStatusCode (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die den aktuellen Status einer Sitzungsressource angeben. Alle Dienstanbieter legen Statuscodes wie MAPI zum Melden des Status des Subsystems, des MAPI-Spoolers und des integrierten Adressbuchs ein.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS_CODE  <br/> |
|Kennung:  <br/> |0x3E04  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Statuscode muss für alle Anbieter in der Datei Mapisvc.inf angezeigt werden. 
  
Statusobjekte werden von MAPI und von allen Dienstanbietern implementiert. Es gibt zwei Sätze gültiger Werte für Statuscodes, eine für alle Statusobjekte und eine andere nur für Transportanbieter. Alle Statusobjekte können diese Eigenschaft auf die folgenden Werte festlegen:
  
STATUS_AVAILABLE 
  
> Gibt an, dass die Ressource betriebsbereit ist.
    
STATUS_FAILURE 
  
> Gibt an, dass bei der Ressource ein Problem auftritt. Bei Dienstanbietern STATUS_FAILURE, dass der Anbieter möglicherweise bald heruntergefahren wird, um die aktuelle Sitzung zu beenden.
    
STATUS_OFFLINE 
  
> Gibt an, dass nur lokale Daten oder Dienste verfügbar sind.
    
Transportanbieter können die Eigenschaften ihrer Statusobjekte **PR_STATUS_CODE** folgenden Werten festlegen: 
  
STATUS_INBOUND_ACTIVE 
  
> Gibt an, dass der Transportanbieter eine eingehende Nachricht empfängt. 
    
STATUS_INBOUND_ENABLED 
  
> Gibt an, dass der Transportanbieter eingehende Nachrichten empfangen kann.
    
STATUS_INBOUND_FLUSH 
  
> Gibt an, dass der Transportanbieter Nachrichten aus der eingehenden Warteschlange herunterloaden wird.
    
STATUS_OUTBOUND_ACTIVE 
  
> Gibt an, dass der Transportanbieter eine ausgehende Nachricht empfängt. 
    
STATUS_OUTBOUND_ENABLED 
  
> Gibt an, dass der Transportanbieter ausgehende Nachrichten verarbeiten kann.
    
STATUS_OUTBOUND_FLUSH 
  
> Gibt an, dass der Transportanbieter Nachrichten aus seiner ausgehenden Warteschlange hochladet.
    
STATUS_REMOTE_ACCESS 
  
> Gibt an, dass der Transportanbieter den Remotezugriff unterstützt.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagStatusString (kanonische Eigenschaft)](pidtagstatusstring-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

