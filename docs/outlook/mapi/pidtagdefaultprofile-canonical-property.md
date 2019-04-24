---
title: Kanonische Pidtagdefaultprofile (-Eigenschaft
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
ms.openlocfilehash: 8295ae6904f503ca831a00c1f35ac08596b5358c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270000"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Kanonische Pidtagdefaultprofile (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Messaging-Benutzerprofil das MAPI-Standardprofil ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Kennung:  <br/> |0x3D04  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nicht als Eigenschaft eines Objekts, sondern nur als Spalte in einer Profiltabelle angezeigt. Eine Clientanwendung kann die [IProfAdmin:: SetDefaultProfile](iprofadmin-setdefaultprofile.md) -Methode verwenden, um das Standardprofil festzulegen. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagdefaultstore (-Eigenschaft](pidtagdefaultstore-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

