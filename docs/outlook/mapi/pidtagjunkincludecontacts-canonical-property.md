---
title: PidTagJunkIncludeContacts (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: df31fbcfd5f238c99e4b5a82771cea1bccf0403f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595231"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>PidTagJunkIncludeContacts (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob E-Mail-Adressen der Kontakte im Ordner "Kontakte" speziell im Hinblick auf den Spamfilter behandelt werden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Kennung:  <br/> |0x6100  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Bei Festlegung auf "0x00000001" müssen diese E-Mail-Adressen den Teil "vertrauenswürdige" E-Mail-Adresse des Junk-E-Mail-Regeleinschränkung auffüllen, sodass E-Mails von diesen Adressen als "nicht Junk" behandelt werden. Bei Festlegung auf "0x00000000" dürfen E-Mail-Adressen aus dem Ordner "Kontakte" nicht zur Junk-E-Mail-Regel hinzugefügt werden, und der Abschnitt der Regel muss NULL sein.
  
Wenn diese Eigenschaft mit dem Wert "0x00000001" vorhanden ist und der hinzugefügte Kontakt E-Mail-Adressen enthält, die noch nicht im Abschnitt "Vertrauenswürdige Kontakte" der Junk-E-Mail-Regel enthalten sind, müssen diese E-Mail-Adressen der Einschränkung hinzugefügt werden. Wenn diese Eigenschaft "0x00000000" ist, ist keine Aktion erforderlich.
  
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

