---
title: PidTagExtendedRuleSizeLimit (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 380fbaf02cbbe4eeac463cedbe6f893cc5f5b54c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563581"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a>PidTagExtendedRuleSizeLimit (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die maximale Größe in Byte, die der Benutzer für eine einzelne "erweiterte" Regel ansammeln darf.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXTENDED_RULE_SIZE_LIMIT  <br/> |
|Kennung:  <br/> |0x0E9B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Regeln  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft für das Anmeldeobjekt festgelegt ist, sollte der Client die Größe der **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) -Eigenschaft unter dem durch diese Eigenschaft angegebenen Wert beibehalten. Umgekehrt sollte der Server einen Fehler zurückgeben, wenn der Client versucht, eine zu große binäre Eigenschaft festzulegen.
  
Informationen zu erweiterten Regeln finden Sie unter [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt zulässige Vorgänge für die zentralen Nachrichtenspeicherobjekte an.
    
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

