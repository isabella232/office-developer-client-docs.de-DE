---
title: PidTagDeferredSendNumber (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3e03f3762f913beb290147b9395fd3c5367d4a55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613541"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>PidTagDeferredSendNumber (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Zahl, die verwendet werden kann, um die Verzögerung des Sendens einer Nachricht zu berechnen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|Kennung:  <br/> |0x3FEB  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird zum Berechnen der **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) -Eigenschaft verwendet, wenn sie nicht vorhanden ist. Wenn das Senden einer Nachricht verzögert wird, sollte die **PR_DEFERRED_SEND_NUMBER-Eigenschaft** zusammen mit der **eigenschaft PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) festgelegt werden, wenn die **PR_DEFERRED_SEND_TIME-Eigenschaft** nicht vorhanden ist. 
  
Der **wert PR_DEFERRED_SEND_NUMBER** muss zwischen 0 und 999 festgelegt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

