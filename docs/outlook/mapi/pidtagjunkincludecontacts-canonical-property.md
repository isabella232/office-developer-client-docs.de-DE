---
title: Kanonische Pidtagjunkincludecontacts (-Eigenschaft
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
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328714"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Kanonische Pidtagjunkincludecontacts (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob die e-Mail-Adressen der Kontakte im Ordner "Kontakte" speziell im Hinblick auf den Spamfilter behandelt werden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Kennung:  <br/> |0x6100  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bei Festlegung auf "0x00000001" müssen diese e-Mail-Adressen den Teil "vertrauenswürdige" Kontakt-e-Mail-Adresse der Junk-e-Mail-Regel Einschränkung auffüllen, sodass e-Mails von diesen Adressen als "kein Junk" behandelt werden. Bei Festlegung auf "0x00000000" dürfen e-Mail-Adressen aus dem Ordner "Kontakte" nicht der Junk-e-Mail-Regel hinzugefügt werden, und der Abschnitt der Regel muss NULL sein.
  
Wenn diese Eigenschaft mit dem Wert "0x00000001" vorhanden ist und der hinzugefügte Kontakt über e-Mail-Adressen verfügt, die noch nicht im Abschnitt vertrauenswürdige Kontakte der Junk-e-Mail-Regel enthalten sind, müssen diese e-Mail-Adressen der Einschränkung hinzugefügt werden. Wenn diese Eigenschaft "0x00000000" ist, ist keine Aktion erforderlich.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.
    
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

