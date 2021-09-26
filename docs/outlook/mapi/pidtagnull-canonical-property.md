---
title: PidTagNull (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c823a9a9ffe17bd466e166ede13d7f7ede25e1e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583324"
---
# <a name="pidtagnull-canonical-property"></a>PidTagNull (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt einen NULL-Wert oder eine Einstellung einer Eigenschaft dar oder reserviert Array-Speicherplatz.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NULL  <br/> |
|Kennung:  <br/> |0x0000  <br/> |
|Datentyp:  <br/> |PT_NULL  <br/> |
|Bereich:  <br/> |Standard  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird verwendet, um Platz in Arrays von [SPropValue-Strukturen](spropvalue.md) zu reservieren. Es wird in einem Array von [SPropTagArray-Strukturen](sproptagarray.md) verwendet, um die Methode anweisen, Speicherplatz im zurückgegebenen Array von **SPropValue-Strukturen** zu reservieren. Auf diese Weise können berechnete Eigenschaften auf kostengünstige Weise ausgefüllt werden. 
  
Weitere Informationen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

