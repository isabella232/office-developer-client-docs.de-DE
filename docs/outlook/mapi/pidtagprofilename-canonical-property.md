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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794820"
---
# <a name="pidtagprofilename-canonical-property"></a>PidTagProfileName (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält den Namen des Profils an.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Bezeichner:  <br/> |0x3D12  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil-Konfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden von Dienstanbietern berechnet. Implementierung der Funktion **ServiceEntry** eines Anbieters kann diese Eigenschaften verwenden, um den Profilnamen zu ermitteln. 
  
Clientanwendungen können diese Eigenschaften als eine praktische Alternative zum Abrufen von den Namen des Profils durch Untersuchen der Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in der MAPI-Subsystems Status Tabellenzeile.
  
Diese Eigenschaften möglicherweise nicht eindeutig über die Zeit, zum Beispiel, in dem ein Profil gelöscht und später erneut mit dem gleichen Namen erstellt. MAPI stellt eine vollständig eindeutige **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))-Eigenschaft im Profilabschnitt hartcodierte bereit **MUID_PROFILE_INSTANCE.**
  
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

