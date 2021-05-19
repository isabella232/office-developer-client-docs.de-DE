---
title: PidTagProfileName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435649"
---
# <a name="pidtagprofilename-canonical-property"></a>PidTagProfileName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen des Profils.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Kennung:  <br/> |0x3D12  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften werden von Dienstanbietern berechnet. Die Implementierung der **ServiceEntry-Funktion** eines Anbieters kann diese Eigenschaften verwenden, um den Profilnamen zu ermitteln. 
  
Clientanwendungen können diese Eigenschaften als bequeme Alternative zum Abrufen des Profilnamens verwenden, indem sie die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft in der Statustabelle des #A0 untersuchen.
  
Diese Eigenschaften sind möglicherweise nicht zeitübergreifend eindeutig, z. B. wenn ein Profil gelöscht und später mit demselben Namen neu erstellt wird. MAPI bietet eine völlig eindeutige **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) -Eigenschaft in einem hart codierten Profilabschnitt **namens MUID_PROFILE_INSTANCE.**
  
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

