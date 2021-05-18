---
title: PidTagNull (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329267"
---
# <a name="pidtagnull-canonical-property"></a>PidTagNull (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt einen Nullwert oder eine Einstellung einer Eigenschaft dar oder reserviert Arraybereich.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NULL  <br/> |
|Kennung:  <br/> |0x0000  <br/> |
|Datentyp:  <br/> |PT_NULL  <br/> |
|Bereich:  <br/> |Standard  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird verwendet, um Speicherplatz in Arrays von [SPropValue-Strukturen zu](spropvalue.md) reservieren. Es wird in einem Array von [SPropTagArray-Strukturen](sproptagarray.md) verwendet, um der Methode zu sagen, dass platz im zurückgegebenen Array von **SPropValue-Strukturen reserviert werden** soll. Dadurch können berechnete Eigenschaften kostengünstig ausgefüllt werden. 
  
Weitere Informationen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

