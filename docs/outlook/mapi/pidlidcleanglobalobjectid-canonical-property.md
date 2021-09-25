---
title: Kanonische PidLidCleanGlobalObjectId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a81d6e0011ba6d4c873cc9eeef3bf81212faec09
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555895"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>Kanonische PidLidCleanGlobalObjectId-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Specifies the clean global **ObjectID**.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidCleanGlobalObjId  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x00000023  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Format dieser Eigenschaft entspricht dem von **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)). Der Wert dieser Eigenschaft muss dem Wert von **LID_GLOBAL_OBJID** entsprechen, außer dass die Felder YH, YL, M und D null sein müssen. Alle Objekte, die auf eine Instanz einer Terminserie (einschließlich einer verwaisten Instanz) sowie auf die Serienserie selbst verweisen, haben denselben Wert für diese Eigenschaft.
  
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

