---
title: Kanonische PidTagProfileName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 65c2f1491be5205b3dadeb6c32d59e77be9bfda2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591690"
---
# <a name="pidtagprofilename-canonical-property"></a>Kanonische PidTagProfileName-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen des Profils.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Kennung:  <br/> |0x3D12  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften werden von Dienstanbietern berechnet. Die Implementierung der **ServiceEntry-Funktion** eines Anbieters kann diese Eigenschaften verwenden, um den Profilnamen zu ermitteln. 
  
Clientanwendungen können diese Eigenschaften als bequeme Alternative zum Abrufen des Profilnamens verwenden, indem sie die **Eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in der Statustabellenzeile des MAPI-Subsystems untersuchen.
  
Diese Eigenschaften sind möglicherweise nicht über einen Zeitraum eindeutig, z. B. wenn ein Profil gelöscht und später mit demselben Namen neu erstellt wird. MAPI stellt eine völlig eindeutige **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) -Eigenschaft in einem hartcodierten Profilabschnitt **namens MUID_PROFILE_INSTANCE bereit.**
  
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

