---
title: PidTagAttachMimeTag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327244"
---
# <a name="pidtagattachmimetag-canonical-property"></a>PidTagAttachMimeTag (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Formatierungsinformationen zu einer Multipurpose Internet Mail Extensions (MIME)-Anlage. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W  <br/> |
|Kennung:  <br/> |0x370E  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) den Wert **OID_MIMETAG** enthält, sollte der Transportanbieter diese Eigenschaften überprüfen, um zu bestimmen, wie die Anlage formatiert wird. 
  
Diese Eigenschaften werden aus dem Parameter Content-type des eingehenden MIME-Headers kopiert. Die Zusammensetzung der Zeichenfolge wird im RFC 1521-Dokument definiert. Das Format ist Typ/Untertyp, z. B. Application/Binary oder Text/Plain. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von mit Rechten verwalteten codierten Nachrichten an.
    
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

