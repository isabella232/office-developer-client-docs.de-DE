---
title: Kanonische pidlidbusinesscardcardpicture (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fd1ad923acca5a75d06e6b15ae7ae7411edefb92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342007"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a>Kanonische pidlidbusinesscardcardpicture (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das Bild, das auf einer Visitenkarte verwendet werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidBCCardPicture  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Address  <br/> |
|Lange ID (LID):  <br/> |0x00008041  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft muss entweder ein Portable Network Graphics (PNG) oder JPEG-Datenstrom sein. Diese Eigenschaft sollte in Verbindung mit der **dispidBCDisplayDefinition** ([pidlidbusinesscarddisplaydefinition (](pidlidbusinesscarddisplaydefinition-canonical-property.md))-Eigenschaft wie folgt verwendet werden: **dispidBCCardPicture** sollte auf einem Kontakt nicht vorhanden sein, wenn ** dispidBCDisplayDefinition** ist nicht vorhanden. Diese Eigenschaft sollte auch nicht vorhanden sein, wenn für die Daten in **dispidBCCardPicture** kein Kartenbild erforderlich ist. 
  
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

