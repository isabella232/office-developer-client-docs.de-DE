---
title: PidTagSearchFolderTemplateId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336624"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>PidTagSearchFolderTemplateId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die ID der Vorlage, die für die Suche verwendet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|Kennung:  <br/> |0x6841  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Suche  <br/> |
   
## <a name="remarks"></a>Hinweise

Suchordnerkriterien werden durch eine Vorlage angegeben. Diese Eigenschaft für die Nachricht, die den Suchordner definiert, identifiziert die entsprechende Vorlage. Neben dem Definieren von Suchkriterien definiert eine Vorlage auch Ordner, die von der Suche ausgeschlossen werden sollen, definiert Elemente, die von der Suche ausgeschlossen werden sollen, und gibt den Wert von **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)) an.
  
Weitere Informationen zu Suchordnervorlagen finden Sie [unter [MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) . 
  
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

