---
title: Kanonische PidTagStatusCode-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fcd890f9fa7055abfd4eb6765434992e758ecb32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599396"
---
# <a name="pidtagstatuscode-canonical-property"></a>Kanonische PidTagStatusCode-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die den aktuellen Status einer Sitzungsressource angeben. Alle Dienstanbieter legen Statuscodes wie die MAPI fest, um den Status des Subsystems, des MAPI-Spoolers und des integrierten Adressbuchs zu melden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS_CODE  <br/> |
|Kennung:  <br/> |0x3E04  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Statuscode muss in der Datei Mapisvc.inf für alle Anbieter angezeigt werden. 
  
Statusobjekte werden von der MAPI und von allen Dienstanbietern implementiert. Es gibt zwei Sätze gültiger Werte für Statuscodes, einen Satz für alle Statusobjekte und einen weiteren nur für Transportanbieter. Alle Statusobjekte können diese Eigenschaft auf die folgenden Werte festlegen:
  
STATUS_AVAILABLE 
  
> Gibt an, dass die Ressource betriebsbereit ist.
    
STATUS_FAILURE 
  
> Gibt an, dass für die Ressource ein Problem auftritt. Bei Dienstanbietern gibt STATUS_FAILURE an, dass der Anbieter möglicherweise bald heruntergefahren wird, um die aktuelle Sitzung zu beenden.
    
STATUS_OFFLINE 
  
> Gibt an, dass nur lokale Daten oder Dienste verfügbar sind.
    
Transportanbieter können auch die **PR_STATUS_CODE** Eigenschaften ihrer Statusobjekte auf die folgenden Werte festlegen: 
  
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
  
> Gibt an, dass der Transportanbieter Nachrichten aus seiner ausgehenden Warteschlange hochlädt.
    
STATUS_REMOTE_ACCESS 
  
> Gibt an, dass der Transportanbieter den Remotezugriff unterstützt.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagStatusString-Eigenschaft](pidtagstatusstring-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

