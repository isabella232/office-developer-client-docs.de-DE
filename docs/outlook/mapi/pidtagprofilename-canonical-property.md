---
title: Kanonische PidTagProfileName-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341650"
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
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden von Dienstanbietern berechnet. Die Implementierung der **ServiceEntry** -Funktion eines Anbieters kann diese Eigenschaften verwenden, um den Profilnamen zu ermitteln. 
  
Client Anwendungen können diese Eigenschaften als bequeme Alternative zum Abrufen des Profilnamens verwenden, indem Sie die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft in der Statustabellen Zeile des MAPI-Subsystems untersuchen.
  
Diese Eigenschaften sind möglicherweise nicht über die Zeit hinweg eindeutig, beispielsweise, wenn ein Profil gelöscht und später mit demselben Namen neu erstellt wird. MAPI liefert eine vollständig eindeutige **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Eigenschaft in einem hartcodierten Profil Abschnitt namens **MUID_PROFILE_INSTANCE.**
  
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

