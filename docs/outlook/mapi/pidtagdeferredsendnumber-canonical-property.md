---
title: Kanonische Pidtagdeferredsendnumber (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9e3a30dad433b255573e4e3f041e6475b9227a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357736"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>Kanonische Pidtagdeferredsendnumber (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Zahl, die zum Berechnen der Verschiebung des Sendens einer Nachricht verwendet werden kann.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|Kennung:  <br/> |0x3FEB  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird zum Berechnen der **PR_DEFERRED_SEND_TIME** ([pidtagdeferredsendtime (](pidtagdeferredsendtime-canonical-property.md))-Eigenschaft verwendet, wenn Sie nicht vorhanden ist. Wenn eine Nachricht verzögert wird, sollte die **PR_DEFERRED_SEND_NUMBER** -Eigenschaft zusammen mit der **PR_DEFERRED_SEND_UNITS** ([pidtagdeferredsendunits (](pidtagdeferredsendunits-canonical-property.md))-Eigenschaft festgelegt werden, wenn die **PR_DEFERRED_SEND_TIME** -Eigenschaft nicht vorhanden ist. 
  
Der **PR_DEFERRED_SEND_NUMBER** -Wert muss zwischen 0 und 999 festgelegt werden. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

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

