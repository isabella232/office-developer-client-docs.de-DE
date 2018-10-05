---
title: PidTagRuleId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398059"
---
# <a name="pidtagruleid-canonical-property"></a>PidTagRuleId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen eindeutigen Bezeichner, den der messaging-Server für jede Regel generiert wird, wenn die Regel erstellt wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_ID  <br/> |
|Kennung:  <br/> |0x6674  <br/> |
|Datentyp:  <br/> |PT_I8  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Client muss diese Eigenschaft nicht angeben, beim Erstellen einer neuen Regel, jedoch müssen sie beim Ändern oder Löschen einer Regel angeben.
  
Wenn eine Regel zu löschen, die einzige Eigenschaft, die der Client weitergeben muss **PR_RULE_ID** und sollte nicht in anderen-Eigenschaft übergeben. Der Server muss Eigenschaften als diese Eigenschaft ignoriert. Hinzufügen einer Regel der Client muss nicht **PR_RULE_ID**übergeben, müssen sie in der **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) und **PR_RULE_PROVIDER** ([ übergeben PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) Eigenschaften. Beim Ändern einer Regel wird der Client muss **PR_RULE_ID** übergeben und übergeben sollten Sie den Rest der Eigenschaften, die geändert werden müssen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagRuleCondition (kanonische Eigenschaft)](pidtagrulecondition-canonical-property.md)
  
[PidTagRuleActions (kanonische Eigenschaft)](pidtagruleactions-canonical-property.md)
  
[PidTagRuleProvider (kanonische Eigenschaft)](pidtagruleprovider-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

