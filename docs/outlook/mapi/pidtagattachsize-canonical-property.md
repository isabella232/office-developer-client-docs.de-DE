---
title: PidTagAttachSize (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4954ab76923e1d6fd9cabb055b74e305b1dec6d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600435"
---
# <a name="pidtagattachsize-canonical-property"></a>PidTagAttachSize (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Summe (in Byte) der Größen aller Eigenschaften einer Anlage. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_SIZE  <br/> |
|Kennung:  <br/> |0x0E20  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es wird empfohlen, dass Anlagenunterobjekte die **PR_ATTACH_SIZE-Eigenschaft** verfügbar machen. Die summe in **PR_ATTACH_SIZE** enthält die Größe der **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft. Entsprechend ist **PR_ATTACH_SIZE** in der Regel größer als der Inhalt der Anlage allein. 
  
Diese Eigenschaft kann verwendet werden, um die ungefähre Größe der Anlage zu überprüfen, bevor eine Remoteübertragung per Modem ausgeführt wird, und um Statusanzeigen anzuzeigen, wenn die Anlage auf dem Datenträger gespeichert wird. Dies ist besonders nützlich bei angefügten OLE-Objekten. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagMessageSize (kanonische Eigenschaft)](pidtagmessagesize-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

