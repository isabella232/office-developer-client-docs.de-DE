---
title: PidTagRecipientReassignmentProhibited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3badd32eb0cf99e512754635b55fc40d08192b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624657"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>PidTagRecipientReassignmentProhibited (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das Hinzufügen zusätzlicher Empfänger beim Weiterleiten der Nachricht für die E-Mail-Nachricht unzulässig ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Kennung:  <br/> |0x002B  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird basierend auf dem **wert PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) der E-Mail-Nachricht festgelegt. Wenn **PR_SENSITIVITY** auf "0x00000000" (normal) oder "0x00000003" (vertraulich) festgelegt ist, muss diese Eigenschaft auf "0x00" oder nicht festgelegt werden, was bedeutet, dass das Hinzufügen zusätzlicher oder anderer Empfänger zur E-Mail-Nachricht zulässig ist. Wenn die **PR_SENSITIVITY** des E-Mail-Objekts auf "0x00000001" (persönlich) oder "0x00000002" (privat) festgelegt ist, muss diese Eigenschaft auf "0x01" festgelegt werden, um zu verhindern, dass zusätzliche oder andere Empfänger dieser E-Mail durch Weiterleitung hinzugefügt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

