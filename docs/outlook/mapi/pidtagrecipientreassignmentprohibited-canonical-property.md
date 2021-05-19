---
title: PidTagRecipientReassignmentProhibited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341111"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>PidTagRecipientReassignmentProhibited (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das Hinzufügen zusätzlicher Empfänger beim Weiterleiten der Nachricht für die E-Mail-Nachricht nicht zulässig ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Kennung:  <br/> |0x002B  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird basierend auf dem Wert PR_SENSITIVITY **(** [PidTagSensitivity](pidtagsensitivity-canonical-property.md)) der E-Mail-Nachricht festgelegt. Wenn **PR_SENSITIVITY** auf "0x00000000" (normal) oder "0x00000003" (vertraulich) festgelegt ist, muss diese Eigenschaft auf "0x00" oder nicht festgelegt sein, was bedeutet, dass das Hinzufügen zusätzlicher oder anderer Empfänger zur E-Mail-Nachricht zulässig ist. Wenn die PR_SENSITIVITY  des E-Mail-Objekts auf "0x00000001" (persönlich) oder "0x00000002" (privat) festgelegt ist, muss diese Eigenschaft "0x01" festgelegt werden, um zu verhindern, dass zusätzliche oder andere Empfänger dieser E-Mail durch Weiterleitung hinzugefügt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

