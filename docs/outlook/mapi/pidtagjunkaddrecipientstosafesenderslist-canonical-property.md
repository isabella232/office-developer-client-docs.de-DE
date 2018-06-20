---
title: Kanonische PidTagJunkAddRecipientsToSafeSendersList-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794530"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Kanonische PidTagJunkAddRecipientsToSafeSendersList-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt an, ob die e-Mail-Empfänger werden, die Liste sicherer Absender hinzugefügt werden soll.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Bezeichner:  <br/> |0x6103  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn dieser Parameter angegeben wurde, muss diese Eigenschaft auf 0 oder 1 festgelegt. Der Wert 1 gibt an, dass die e-Mail-Empfänger werden, die Liste sicherer Absender hinzugefügt werden soll. Der Wert 0 gibt an, dass die e-Mail-Empfänger werden nicht für die Liste sicherer Absender hinzugefügt werden.
  
Wenn diese Eigenschaft mit einem Wert von 1 vorhanden ist, müssen die SMTP-Adressen der e-Mail-Empfänger vertrauenswürdigen Absender-Klausel der Junk-e-Mail-Regel Bedingung hinzugefügt werden. Wenn diese Eigenschaft 0 ist, ist keine Aktion erforderlich.
  
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

