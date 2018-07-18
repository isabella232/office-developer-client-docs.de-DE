---
title: PidLidBusinessCardDisplayDefinition (kanonische Eigenschaft)
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 34d29b9a15cc6f5a3f88a6477738eb63904e1fdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793462"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>PidLidBusinessCardDisplayDefinition (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält benutzeranpassungen Details für einen Kontakt als Visitenkarte anzeigen.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidBCDisplayDefinition  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Address  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008040  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Layout einer Visitenkarte kann als ein Bild und eine Reihe von Textfeldern dargestellt werden. Das Bild kann entweder ein Foto des Kontakts oder ein Bild der Visitenkarte sein. Textfelder bestehen einen Wert aus einer anderen-Eigenschaft auf den Kontakt festlegen und eine optionale benutzerdefinierte Bezeichnung-Zeichenfolge, die vom Benutzer bereitgestellten. Beachten Sie, dass Sie Multibyte-Werte in little-Endian-Format im Puffer gespeichert sind.
  
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

