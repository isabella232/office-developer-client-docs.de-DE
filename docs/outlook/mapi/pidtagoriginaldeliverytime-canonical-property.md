---
title: Kanonische Pidtagoriginaldeliverytime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bbe277092b450a4254e02d00d2cf54e35ec6be44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355657"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a>Kanonische Pidtagoriginaldeliverytime (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Kopie der Übermittlungsdatum und-Uhrzeit der ursprünglichen Nachricht in einem Thread. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_DELIVERY_TIME  <br/> |
|Kennung:  <br/> |0x0055  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird von der ursprünglichen **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))-Eigenschaft in nachfolgenden Reply-oder Forward-Vorgängen kopiert und in Lese-und nonread-Berichten verwendet. Zuzustellenden Berichte verwenden Sie stattdessen die **PR_DELIVER_TIME** ([pidtagdelivertime (](pidtagdelivertime-canonical-property.md))-Eigenschaft.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

