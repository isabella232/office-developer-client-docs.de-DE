---
title: PidTagJunkIncludeContacts (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4dde93bbec2594804ab18a3ee4eb3e116a57e528
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794537"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>PidTagJunkIncludeContacts (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt an, ob e-Mail-Adressen der Kontakte im Ordner Kontakte speziell in Bezug auf den Spam-Filter behandelt werden.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Bezeichner:  <br/> |0x6100  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie auf "0 x 00000001" festgelegt ist, diese e-Mail-Adressen den "vertrauenswürdigen" Kontakt-e-Mail-Adressteil der Junk-e-Mail Regel Einschränkung auffüllen müssen so, dass e-Mails von diesen Adressen als "kein junk" behandelt wird. Wenn auf "0 x 00000000" gesetzt, e-Mail-Adressen aus dem Ordner Kontakte nicht hinzugefügt werden die Regel für Junk-e-Mail müssen und im Abschnitt der Regel muss NULL sein.
  
Wenn diese Eigenschaft vorhanden, mit dem Wert "0 x 00000001" und ist weist der hinzugefügte Kontakt e-Mail-Adressen, die noch nicht im Abschnitt vertrauenswürdige Kontakte von der Regel für Junk-e-Mail enthalten sind, müssen diese e-Mail-Adressen die Beschränkung hinzugefügt werden. Wenn diese Eigenschaft auf "0 x 00000000" ist, ist keine Aktion erforderlich.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.
    
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

