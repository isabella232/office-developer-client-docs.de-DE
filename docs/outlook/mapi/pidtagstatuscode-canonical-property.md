---
title: Kanonische Pidtagstatuscode (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278757"
---
# <a name="pidtagstatuscode-canonical-property"></a>Kanonische Pidtagstatuscode (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die den aktuellen Status einer Sitzungs Ressource kennzeichnen. Alle Dienstanbieter legen Statuscodes fest, ebenso wie MAPI, um den Status des Subsystems, den MAPI-Spooler und das integrierte Adressbuch zu melden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS_CODE  <br/> |
|Kennung:  <br/> |0x3E04  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Statuscode muss in der Datei MAPISVC. inf für alle Anbieter angezeigt werden. 
  
Status Objekte werden von MAPI und von allen Dienstanbietern implementiert. Es gibt zwei Sätze gültiger Werte für Statuscodes, ein Satz für alle Status-Objekte und ein weiterer Satz nur für Transportanbieter. Alle Status-Objekte können diese Eigenschaft auf die folgenden Werte festlegen:
  
STATUS_AVAILABLE 
  
> Gibt an, dass die Ressource betriebsbereit ist.
    
STATUS_FAILURE 
  
> Gibt an, dass die Ressource ein Problem aufWeist. Für Dienstanbieter gibt STATUS_FAILURE an, dass der Anbieter in Kürze heruntergefahren werden kann, um die aktuelle Sitzung zu beenden.
    
STATUS_OFFLINE 
  
> Gibt an, dass nur lokale Daten oder Dienste verfügbar sind.
    
Transport Anbieter können auch die **PR_STATUS_CODE** -Eigenschaften ihrer Statusobjekte auf die folgenden Werte festlegen: 
  
STATUS_INBOUND_ACTIVE 
  
> Gibt an, dass der Transportanbieter eine eingehende Nachricht empfängt. 
    
STATUS_INBOUND_ENABLED 
  
> Gibt an, dass der Transportanbieter eingehende Nachrichten empfangen kann.
    
STATUS_INBOUND_FLUSH 
  
> Gibt an, dass der Transportanbieter Nachrichten aus der eingehenden Warteschlange herunterlädt.
    
STATUS_OUTBOUND_ACTIVE 
  
> Gibt an, dass der Transportanbieter eine ausgehende Nachricht empfängt. 
    
STATUS_OUTBOUND_ENABLED 
  
> Gibt an, dass der Transportanbieter ausgehende Nachrichten verarbeiten kann.
    
STATUS_OUTBOUND_FLUSH 
  
> Gibt an, dass der Transportanbieter Nachrichten aus der ausgehenden Warteschlange hoch lädt.
    
STATUS_REMOTE_ACCESS 
  
> Gibt an, dass der Transportanbieter den Remotezugriff unterstützt.
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagstatusstring (-Eigenschaft](pidtagstatusstring-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

