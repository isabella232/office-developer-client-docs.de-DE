---
title: PidTagAutoForwarded (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326614"
---
# <a name="pidtagautoforwarded-canonical-property"></a>PidTagAutoForwarded (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Client ein X-MS-Exchange-Organization-AutoForwarded-Kopfzeilenfeld anfordert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AUTO_FORWARDED  <br/> |
|Kennung:  <br/> |0x0005  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Allgemeine Berichterstellung  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft auf FALSE festgelegt ist oder nicht verwendet wird, wird kein X-MS-Exchange-Organization-AutoForwarded-Kopfzeilenfeld erstellt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Definiert jede Eigenschaft, die in den Objekten verwendet wird, die von DOKUMENTEN mit MS-OXO-Präfix beschrieben werden.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
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

