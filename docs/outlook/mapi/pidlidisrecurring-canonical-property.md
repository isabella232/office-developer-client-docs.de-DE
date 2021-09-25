---
title: Kanonische PidLidIsRecurring-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f06abd2db992f68b07c2dcbf663f4263c164e073
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583786"
---
# <a name="pidlidisrecurring-canonical-property"></a>Kanonische PidLidIsRecurring-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das Objekt einer Terminserie zugeordnet ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |LID_IS_RECURRING  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x00000005  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert TRUE gibt an, dass das Objekt eine Serienserie oder eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt. Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass das Objekt eine einzelne Instanz darstellt. Beachten Sie den Unterschied zwischen dieser Eigenschaft und der **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) -Eigenschaft.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

