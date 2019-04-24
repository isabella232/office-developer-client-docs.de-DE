---
title: Kanonische Pidlidhaspicture (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHasPicture
api_type:
- COM
ms.assetid: c3bea11c-3197-4060-8672-f1b4bf352112
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357750"
---
# <a name="pidlidhaspicture-canonical-property"></a>Kanonische Pidlidhaspicture (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob eine Foto Anlage für einen Kontakt vorhanden ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidHasPicture  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long-ID (Deckel):  <br/> |0x00008015  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft vorhanden ist und auf TRUE festgelegt ist, enthält die Attachment-Tabelle des Kontakts eine Anlage, wobei die **PR_ATTACHMENT_CONTACTPHOTO** ([pidtagattachmentcontactphoto (](pidtagattachmentcontactphoto-canonical-property.md))-Eigenschaft auf true festgelegt ist.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

