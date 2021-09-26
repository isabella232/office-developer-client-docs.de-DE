---
title: PidTagServiceExtraUids (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 411adc200d4b337eaaa6b51e47269c0f02d9b899
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624496"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>PidTagServiceExtraUids (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste von [MAPIUID-Strukturen,](mapiuid.md) die zusätzliche Profilabschnitte für den Nachrichtendienst identifizieren. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Kennung:  <br/> |0x3D0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für jeden Nachrichtenfilter können neue Profilabschnitte erstellt werden. Wenn die Informationen zum Nachrichtendienst in ein anderes Profil kopiert werden sollen, ist es wichtig, auch die zusätzlichen Profilabschnitte für die Filter zu kopieren. Ein Dienstanbieter, der zusätzliche Profilabschnitte verwendet, kann die **MAPIUID-Strukturen** dieser Profilabschnitte in **PR_SERVICE_EXTRA_UIDS** speichern, wodurch die MAPI die zusätzlichen Nachrichtendienstinformationen kopieren kann.
  
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

