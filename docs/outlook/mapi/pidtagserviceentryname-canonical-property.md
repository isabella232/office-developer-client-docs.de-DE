---
title: Kanonische Pidtagserviceentryname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432471"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Kanonische Pidtagserviceentryname (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen der Einstiegspunktfunktion für die Konfiguration eines Nachrichtendiensts.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Kennung:  <br/> |0x3D0B  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass der Nachrichtendienst Implementierer einen Einstiegspunkt für den Nachrichtendienst bereitstellt, der Einstiegspunkt ist jedoch nicht erforderlich. Der Einstiegspunkt sollte jedoch nur angegeben werden, wenn die zugehörigen Konfigurationseigenschaften vorhanden sind. Wenn diese Eigenschaften nicht vorhanden sind, geht MAPI davon aus, dass kein Einstiegspunkt bereitgestellt wird.
  
Die Dynamic Link Library (DLL), in der die Einstiegspunktfunktion angezeigt wird, wird von der **PR_SERVICE_DLL_NAME** ([pidtagservicedllname (](pidtagservicedllname-canonical-property.md))-Eigenschaft benannt.
  
Weitere Informationen zu Einstiegspunkten für den Nachrichtendienst finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

