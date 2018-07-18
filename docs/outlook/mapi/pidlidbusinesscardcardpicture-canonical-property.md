---
title: PidLidBusinessCardCardPicture (kanonische Eigenschaft)
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8e241022504291ad70f45a3318a7901bbbba213f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793458"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a>PidLidBusinessCardCardPicture (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält das Bild, das auf einer Visitenkarte verwenden.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidBCCardPicture  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Address  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008041  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft muss entweder ein portable Network Graphics (PNG) oder JPEG-Stream. Diese Eigenschaft sollte in Verbindung mit der **DispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md))-Eigenschaft wie folgt verwendet werden: **DispidBCCardPicture** sollte nicht vorhanden sein, auf einen Kontakt If ** DispidBCDisplayDefinition** ist nicht vorhanden. Diese Eigenschaft sollte auch nicht vorhanden sein, wenn die Daten in **DispidBCCardPicture** Bild einer Karte nicht erforderlich sind. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

