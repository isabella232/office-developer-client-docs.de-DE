---
title: PidTagJunkAddRecipientsToSafeSendersList (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9bad8ceba8bc964fcb1d3c531ccb8a4e9d63d386
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587531"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>PidTagJunkAddRecipientsToSafeSendersList (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob die E-Mail-Empfänger der Liste der sicheren Absender hinzugefügt werden sollen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Kennung:  <br/> |0x6103  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn vorhanden, muss diese Eigenschaft auf 0 oder 1 festgelegt werden. Der Wert 1 gibt an, dass die E-Mail-Empfänger der Liste der sicheren Absender hinzugefügt werden sollen. Der Wert 0 gibt an, dass die E-Mail-Empfänger nicht zur Liste der sicheren Absender hinzugefügt werden sollen.
  
Wenn diese Eigenschaft mit dem Wert 1 vorhanden ist, müssen die SMTP-Adressen der E-Mail-Empfänger der Klausel für vertrauenswürdige Absender der Junk-E-Mail-Regelbedingung hinzugefügt werden. Wenn diese Eigenschaft 0 ist, ist keine Aktion erforderlich.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Zulassungs-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.
    
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

