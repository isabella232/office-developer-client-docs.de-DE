---
title: PidTagSearchAttachments (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336323"
---
# <a name="pidtagsearchattachments-canonical-property"></a>PidTagSearchAttachments (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Unicode-Zeichenfolge, die in Anlageninhalten im Speicher abgefragt wird.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|Kennung:  <br/> |0x0EA5  <br/> |
|Eigenschaftstyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Suche  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

> [!NOTE]
> Dieses MAPI-Einschränkungstag, das bei der Suche nach Anlageninhalten verwendet wird, ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. Sie können sie ihrem Code mithilfe des folgenden Werts hinzufügen: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Microsoft Exchange Server Protokollspezifikationen.
    
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

