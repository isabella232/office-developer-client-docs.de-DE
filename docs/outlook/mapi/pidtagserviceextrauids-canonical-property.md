---
title: Kanonische Pidtagserviceextrauids (-Eigenschaft
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
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328728"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Kanonische Pidtagserviceextrauids (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste von [MAPIUID](mapiuid.md) -Strukturen, die zusätzliche Profilabschnitte für den Nachrichtendienst identifizieren. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Kennung:  <br/> |0x3D0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für jeden Nachrichtenfilter können neue Profilabschnitte erstellt werden. Wenn die Informationen zum Nachrichtendienst in ein anderes Profil kopiert werden sollen, ist es wichtig, auch die zusätzlichen Profilabschnitte für die Filter zu kopieren. Ein Dienstanbieter, der zusätzliche Profilabschnitte verwendet, kann die **MAPIUID** -Strukturen dieser Profilabschnitte in **PR_SERVICE_EXTRA_UIDS**speichern, sodass MAPI die zusätzlichen Informationen zum Nachrichtendienst kopiert.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

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

