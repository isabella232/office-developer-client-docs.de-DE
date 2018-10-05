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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400796"
---
# <a name="pidtagnull-canonical-property"></a>PidTagNull (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt einen null-Wert oder die Einstellung einer Eigenschaft oder Array-Speicherplatz reserviert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NULL  <br/> |
|Kennung:  <br/> |0x0000  <br/> |
|Datentyp:  <br/> |PT_NULL  <br/> |
|Bereich:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird verwendet, um Speicherplatz in Arrays von [SPropValue](spropvalue.md) Strukturen zu reservieren. Es wird in ein Array von [SPropTagArray](sproptagarray.md) Strukturen verwendet, anzuweisen, die Methode, um Speicherplatz im zurückgegebenen Array der **SPropValue** Strukturen zu reservieren. Dies ermöglicht berechnete Eigenschaften in eine kostengünstige Möglichkeit gefüllt werden soll. 
  
Weitere Informationen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die auf Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

