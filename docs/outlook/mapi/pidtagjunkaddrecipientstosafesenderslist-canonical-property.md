---
title: Kanonische Pidtagjunkaddrecipientstosafesenderslist (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282368"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Kanonische Pidtagjunkaddrecipientstosafesenderslist (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob die e-Mail-Empfänger der Liste sicherer Absender hinzugefügt werden sollen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Kennung:  <br/> |0x6103  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sofern vorhanden, muss diese Eigenschaft auf 0 oder 1 festgelegt werden. Der Wert 1 gibt an, dass die e-Mail-Empfänger der Liste sicherer Absender hinzugefügt werden sollen. Der Wert 0 gibt an, dass die e-Mail-Empfänger nicht der Liste der sicheren Absender hinzugefügt werden sollen.
  
Wenn diese Eigenschaft mit dem Wert 1 vorhanden ist, müssen die SMTP-Adressen der e-Mail-Empfänger der Regelbedingung für vertrauenswürdige Absender hinzugefügt werden. Wenn diese Eigenschaft 0 ist, ist keine Aktion erforderlich.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

