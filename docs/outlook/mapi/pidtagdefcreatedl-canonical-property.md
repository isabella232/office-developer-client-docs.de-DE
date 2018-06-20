---
title: Kanonische PidTagDefCreateDl-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794297"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>Kanonische PidTagDefCreateDl-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die Vorlage Eintrags-ID für eine Verteilerliste Standard. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_DEF_CREATE_DL  <br/> |
|Bezeichner:  <br/> |0x3611  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Clientanwendungen mit dieser Eigenschaft können Sie um eine Verteilerliste in einem Container zu erstellen. Unterstützung von Eintrag Creation ist optional für Address Book Container. die, die nicht unterstützen sind nicht erforderlich, diese Eigenschaft verfügbar machen. 
  
Diese Eigenschaft gibt einen Eintrag, der angezeigt werden, kann in der Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) für Verteilerlisten. Wenn den Bezeichner erhalten haben, verwendet der Client es in einem Aufruf der [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode. Der Eintrag stellt die Vorlage für die Standard-Verteilerliste dar. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

