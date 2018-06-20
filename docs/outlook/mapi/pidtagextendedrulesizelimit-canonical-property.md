---
title: Kanonische PidTagExtendedRuleSizeLimit-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794365"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a>Kanonische PidTagExtendedRuleSizeLimit-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die maximale Größe in Bytes, die Benutzer für eine einzelne Regel "Erweiterte" aufgelistet werden.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_EXTENDED_RULE_SIZE_LIMIT  <br/> |
|Bezeichner:  <br/> |0x0E9B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft auf das Anmeldeobjekt festgelegt ist, sollte der Client die Größe der Eigenschaft **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) unter der von dieser Eigenschaft angegebene Wert beibehalten. Dagegen sollte der Server einen Fehler zurück, wenn der Client versucht, eine binäre Eigenschaft festlegen, die zu groß ist.
  
Informationen zu erweiterten Regeln finden Sie unter [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.
    
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

