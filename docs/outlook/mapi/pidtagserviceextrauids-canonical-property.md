---
title: PidTagServiceExtraUids (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422306"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>PidTagServiceExtraUids (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der [MAPIUID-Strukturen,](mapiuid.md) die zusätzliche Profilabschnitte für den Nachrichtendienst identifizieren. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Kennung:  <br/> |0x3D0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Hinweise

Neue Profilabschnitte können für jeden Nachrichtenfilter erstellt werden. Wenn die Informationen zum Nachrichtendienst in ein anderes Profil kopiert werden sollen, ist es wichtig, auch die zusätzlichen Profilabschnitte für die Filter zu kopieren. Ein Dienstanbieter, der zusätzliche Profilabschnitte verwendet, kann die **MAPIUID-Strukturen** dieser Profilabschnitte in **PR_SERVICE_EXTRA_UIDS** speichern, wodurch MAPI die zusätzlichen Nachrichtendienstinformationen kopieren kann.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

