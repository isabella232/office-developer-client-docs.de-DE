---
title: Kanonische PidTagSearchFolderTemplateId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4e752d3264a64ad7b467947c44d01eb7c47ec863
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795126"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>Kanonische PidTagSearchFolderTemplateId-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die ID der Vorlage, die für die Suche verwendet wird.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|Bezeichner:  <br/> |0x6841  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Suchen  <br/> |
   
## <a name="remarks"></a>Hinweise

Ordner Suchkriterien wird durch eine Vorlage angegeben. Diese Eigenschaft für die Nachricht, die den Suchordner definiert identifiziert die zugehörige Vorlage. Zusätzlich zu den Suchkriterien definieren, eine Vorlage auch Ordner, die von der Suche ausschließen definiert, Elemente aus der Suche ausschließen definiert und gibt den Wert des **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).
  
Weitere Informationen zu Search Ordnervorlagen finden Sie unter [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) . 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.
    
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

