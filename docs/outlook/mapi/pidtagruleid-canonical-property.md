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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359493"
---
# <a name="pidtagruleid-canonical-property"></a>PidTagRuleId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen eindeutigen Bezeichner an, den der Messagingserver für jede Regel generiert, wenn die Regel zum ersten Mal erstellt wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_ID  <br/> |
|Kennung:  <br/> |0x6674  <br/> |
|Datentyp:  <br/> |PT_I8  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Client darf diese Eigenschaft beim Erstellen einer neuen Regel nicht angeben, muss sie jedoch beim Ändern oder Löschen einer Regel angeben.
  
Beim Löschen einer Regel muss der Client  nur eine PR_RULE_ID übergeben und darf keine andere Eigenschaft übergeben. Der Server muss andere Eigenschaften als diese Eigenschaft ignorieren. Beim Hinzufügen einer Regel darf der Client PR_RULE_ID nicht **übergeben.** Er muss die **Eigenschaften PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) und **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) übergeben. Beim Ändern einer Regel muss  der Client PR_RULE_ID übergeben und die restlichen Eigenschaften übergeben, die geändert werden müssen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagRuleCondition (kanonische Eigenschaft)](pidtagrulecondition-canonical-property.md)
  
[PidTagRuleActions (kanonische Eigenschaft)](pidtagruleactions-canonical-property.md)
  
[PidTagRuleProvider (kanonische Eigenschaft)](pidtagruleprovider-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

