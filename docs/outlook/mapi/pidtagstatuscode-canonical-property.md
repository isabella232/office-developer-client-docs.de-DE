---
title: Kanonische PidTagStatusCode-Eigenschaft
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
ms.openlocfilehash: efd0dcc8fc01fa433cbbf30936244e4818f8b14a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795207"
---
# <a name="pidtagstatuscode-canonical-property"></a>Kanonische PidTagStatusCode-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Bitmaske der Flags, die den aktuellen Status einer Sitzung Ressource angeben. Alle-Dienstanbieter festzulegen Statuscodes, wie MAPI, um den Bericht über den Status des Teilsystems, die MAPI-Warteschlange und das integrierte-Adressbuch.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_STATUS_CODE  <br/> |
|Bezeichner:  <br/> |0x3E04  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Statuscode muss für alle Anbieter in der Datei "Mapisvc.inf" angezeigt werden. 
  
Status-Objekte werden MAPI und von allen Dienstanbietern implementiert. Es gibt zwei Sätze von gültigen Werten für Statuscodes, eine Gruppe für alle Objekte, Status und einen weiteren Satz für Transportanbieter nur ein. Alle Status-Objekte können diese Eigenschaft auf die folgenden Werte festlegen:
  
STATUS_AVAILABLE 
  
> Gibt an, dass die Ressource ordnungsgemäß funktioniert.
    
STATUS_FAILURE 
  
> Gibt an, dass die Ressource ein Problem aufgetreten ist. Für Dienstanbieter gibt STATUS_FAILURE an, dass der Anbieter bald heruntergefahren werden kann, um die aktuelle Sitzung zu beenden.
    
STATUS_OFFLINE 
  
> Gibt an, dass nur lokale Daten oder Dienste zur Verfügung stehen.
    
Transportanbieter können auch ihr Status des Objekts **PR_STATUS_CODE** Eigenschaften auf die folgenden Werte festlegen: 
  
STATUS_INBOUND_ACTIVE 
  
> Gibt an, dass der Adressbuchhierarchie eine eingehende Nachricht empfangen wird. 
    
STATUS_INBOUND_ENABLED 
  
> Gibt an, dass der Adressbuchhierarchie eingehende Nachrichten empfangen kann.
    
STATUS_INBOUND_FLUSH 
  
> Gibt an, dass der Adressbuchhierarchie aus der Warteschlange für eingehende Nachrichten heruntergeladen wird.
    
STATUS_OUTBOUND_ACTIVE 
  
> Gibt an, dass der Adressbuchhierarchie eine ausgehende Nachricht empfängt. 
    
STATUS_OUTBOUND_ENABLED 
  
> Gibt an, dass der Adressbuchhierarchie ausgehende Nachrichten verarbeitet werden kann.
    
STATUS_OUTBOUND_FLUSH 
  
> Gibt an, dass der Adressbuchhierarchie Nachrichten aus der ausgehenden Warteschlange hochgeladen wird.
    
STATUS_REMOTE_ACCESS 
  
> Gibt an, dass der Adressbuchhierarchie Remotezugriff unterstützt.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagStatusString-Eigenschaft](pidtagstatusstring-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

