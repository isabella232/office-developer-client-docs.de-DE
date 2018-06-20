---
title: Kanonische PidTagServiceExtraUids-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 71f802014200d4b767c346c14df53f1193d44b0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795160"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Kanonische PidTagServiceExtraUids-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Liste von [MAPIUID](mapiuid.md) -Strukturen, die zusätzliche Profil Abschnitte für den Dienst zu identifizieren. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Bezeichner:  <br/> |0x3D0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Hinweise

Neue Profil Abschnitte können für jede Nachrichtenfilter erstellt werden. Wenn die Informationen über den Dienst ist in einem anderen Profil kopiert werden, ist es wichtig, die zusätzliche Profil Abschnitte für die Filter sowie kopieren. Ein Dienstanbieter, der zusätzliche Profil Abschnitten verwendet kann die **MAPIUID** Strukturen Abschnitten Profil in **PR_SERVICE_EXTRA_UIDS**, speichern, die MAPI zum Kopieren von Informationen für den Dienst zusätzliche Nachricht ermöglicht.
  
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

