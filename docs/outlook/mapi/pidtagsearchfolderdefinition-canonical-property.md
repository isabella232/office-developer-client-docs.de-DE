---
title: PidTagSearchFolderDefinition (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b4e5fa7228cf243c79a8ec0c9e2b73b7da21c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336358"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a>PidTagSearchFolderDefinition (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Daten, die die Suchkriterien angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_WB_SF_DEFINITION  <br/> |
|Kennung:  <br/> |0x6845  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Suche  <br/> |
   
## <a name="remarks"></a>Hinweise

Der spezifische Inhalt jedes Felds des binary large object (BLOB), das in dieser Eigenschaft enthalten ist, hängt von der Vorlagen-ID ab, die in **der PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md))-Eigenschaft angegeben ist. Weitere Informationen zur BLOB-Struktur und suchvorlagen finden Sie [unter [MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.
    
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

