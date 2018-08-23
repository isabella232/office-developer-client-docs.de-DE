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
ms.openlocfilehash: 0deb1b34a437d47ab53cdb2e13cda006d9116f65
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570121"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>PidTagServiceExtraUids (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste von [MAPIUID](mapiuid.md) -Strukturen, die zusätzliche Profil Abschnitte für den Dienst zu identifizieren. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Kennung:  <br/> |0x3D0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

