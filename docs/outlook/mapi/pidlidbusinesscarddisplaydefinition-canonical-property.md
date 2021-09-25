---
title: Kanonische PidLidBusinessCardDisplayDefinition-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7c3c2a5e7c575bd6eacd2b8bb66141f1e1864da7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625084"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>Kanonische PidLidBusinessCardDisplayDefinition-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Benutzeranpassungsdetails zum Anzeigen eines Kontakts als Visitenkarte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidBCDisplayDefinition  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008040  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Layout einer Visitenkarte kann als Bild und eine Reihe von Textfeldern dargestellt werden. Das Bild kann ein Kontaktfoto oder ein Kartenbild sein. Textfelder bestehen aus einem Wert aus einer anderen Eigenschaft, die für den Kontakt festgelegt wurde, und einer optionalen benutzerdefinierten Beschriftungszeichenfolge, die vom Benutzer bereitgestellt wird. Beachten Sie, dass Multibytewerte im Little-Endian-Format im Puffer gespeichert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

