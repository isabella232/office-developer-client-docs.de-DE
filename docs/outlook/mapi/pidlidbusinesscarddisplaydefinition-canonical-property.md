---
title: Kanonische pidlidbusinesscarddisplaydefinition (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342035"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>Kanonische pidlidbusinesscarddisplaydefinition (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Details zur Benutzeranpassung zum Anzeigen eines Kontakts als Visitenkarte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidBCDisplayDefinition  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Address  <br/> |
|Lange ID (LID):  <br/> |0x00008040  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Layout einer Visitenkarte kann als Bild und als Anzahl von Textfeldern dargestellt werden. Das Bild kann entweder ein Kontakt Foto oder ein Kartenbild sein. Text Felder bestehen aus einem Wert aus einer anderen für den Kontakt festgelegten Eigenschaft und einer optionalen benutzerdefinierten bezeichnungszeichenfolge, die vom Benutzer bereitgestellt wird. Beachten Sie, dass Multi-Byte-Werte im Little-Endian-Format im Puffer gespeichert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

