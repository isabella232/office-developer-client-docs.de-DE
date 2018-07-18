---
title: PidTagDeferredSendNumber (kanonische Eigenschaft)
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
ms.openlocfilehash: f2ccd004415bcbd42b56b1269fbdb4622ef1f8c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794322"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>PidTagDeferredSendNumber (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Zahl, die zum Berechnen der Aufgeschobene Senden einer Nachricht verwendet werden kann.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|Bezeichner:  <br/> |0x3FEB  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird verwendet, für die Eigenschaft **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) computing, wenn er nicht vorhanden ist. Beim Senden einer Nachricht verzögert ist, sollte die **PR_DEFERRED_SEND_NUMBER** -Eigenschaft zusammen mit der Eigenschaft **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) festgelegt werden, wenn die **PR_DEFERRED_SEND_TIME** -Eigenschaft nicht vorhanden ist. 
  
Der Wert **PR_DEFERRED_SEND_NUMBER** muss zwischen 0 und 999 festgelegt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

