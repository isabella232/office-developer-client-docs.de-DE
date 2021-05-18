---
title: PidTagAttachSize (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361089"
---
# <a name="pidtagattachsize-canonical-property"></a>PidTagAttachSize (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Summe aller Eigenschaften einer Anlage in Bytes. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_SIZE  <br/> |
|Kennung:  <br/> |0x0E20  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Anlagenunterobjekte die PR_ATTACH_SIZE **verfügbar** machen. Die summe in **PR_ATTACH_SIZE** enthält die Größe der **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft. Dementsprechend ist **PR_ATTACH_SIZE** in der Regel größer als der Inhalt der Anlage allein. 
  
Diese Eigenschaft kann verwendet werden, um die ungefähre Größe der Anlage vor der Remoteübertragung per Modem zu überprüfen und Statusanzeigen beim Speichern der Anlage auf dem Datenträger zu zeigen. Dies ist besonders bei angefügten OLE-Objekten hilfreich. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagMessageSize (kanonische Eigenschaft)](pidtagmessagesize-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

