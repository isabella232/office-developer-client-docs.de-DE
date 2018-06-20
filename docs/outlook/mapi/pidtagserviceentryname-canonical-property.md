---
title: Kanonische PidTagServiceEntryName-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795150"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Kanonische PidTagServiceEntryName-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält den Namen der Funktion Punkt Eintrag für die Konfiguration eines Diensts Nachricht.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Bezeichner:  <br/> |0x3D0B  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Message Service Implementierer einen Nachricht Service Einstiegspunkt bereitstellen, aber der Einstiegspunkt nicht erforderlich ist. Der Einstiegspunkt sollten jedoch bereitgestellt werden, nur, wenn die zugehörigen Konfigurationseigenschaften vorhanden. Wenn diese Eigenschaften nicht vorhanden sind, wird MAPI davon ausgegangen, dass kein Einstiegspunkt bereitgestellt wird.
  
Die Dynamic Link Library (DLL) in der die Funktion Eintrag angezeigt wird, heißt von der **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))-Eigenschaft.
  
Weitere Informationen zu Nachricht Service Einstiegspunkte finden Sie unter [Implementieren einer Service Provider Eintrag Point-Funktion](implementing-a-service-provider-entry-point-function.md).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

