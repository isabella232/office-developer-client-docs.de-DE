---
title: PidTagDefaultProfile (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6cd255c60987ec7a279e509aa2925a8029cce62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794272"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>PidTagDefaultProfile (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält True, wenn ein Benutzerprofil messaging das MAPI-Standardprofil ist.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Bezeichner:  <br/> |0x3D04  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nicht als eine Eigenschaft eines Objekts, sondern nur als eine Spalte in einer Profiltabelle angezeigt. Die [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) -Methode können eine Clientanwendung aus das Standardprofil auswählen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagDefaultStore (kanonische Eigenschaft)](pidtagdefaultstore-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

