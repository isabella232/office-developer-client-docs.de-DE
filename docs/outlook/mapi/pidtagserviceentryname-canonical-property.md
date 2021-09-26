---
title: Kanonische PidTagServiceEntryName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 139820a451c17f285bab384a6455ec233b8988b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599417"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Kanonische PidTagServiceEntryName-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen der Einstiegspunktfunktion für die Konfiguration eines Nachrichtendiensts.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Kennung:  <br/> |0x3D0B  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es wird empfohlen, dass Nachrichtendienst-Implementierer einen Einstiegspunkt für den Nachrichtendienst bereitstellen, der Einstiegspunkt ist jedoch nicht erforderlich. Der Einstiegspunkt sollte jedoch nur angegeben werden, wenn die zugehörigen Konfigurationseigenschaften vorhanden sind. Wenn diese Eigenschaften nicht vorhanden sind, geht MAPI davon aus, dass kein Einstiegspunkt bereitgestellt wird.
  
Die Dynamic Link Library (DLL), in der die Einstiegspunktfunktion angezeigt wird, wird durch die **eigenschaft PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) benannt.
  
Weitere Informationen zu Einstiegspunkten des Nachrichtendiensts finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion.](implementing-a-service-provider-entry-point-function.md)
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

