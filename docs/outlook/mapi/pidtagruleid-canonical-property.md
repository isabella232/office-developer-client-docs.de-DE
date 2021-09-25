---
title: PidTagRuleId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b8cca70214543658f708beb81785617d79406c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624559"
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
   
## <a name="remarks"></a>Bemerkungen

Der Client darf diese Eigenschaft beim Erstellen einer neuen Regel nicht angeben, muss sie jedoch beim Ändern oder Löschen einer Regel angeben.
  
Beim Löschen einer Regel ist die einzige Eigenschaft, die der Client übergeben muss, **PR_RULE_ID** und sollte keine andere Eigenschaft übergeben. Der Server muss andere Eigenschaften als diese Eigenschaft ignorieren. Beim Hinzufügen einer Regel darf der Client **PR_RULE_ID** nicht übergeben, er muss die Eigenschaften **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) und **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) übergeben. Beim Ändern einer Regel muss der Client **PR_RULE_ID** übergeben und die restlichen Eigenschaften übergeben, die geändert werden müssen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagRuleCondition (kanonische Eigenschaft)](pidtagrulecondition-canonical-property.md)
  
[PidTagRuleActions (kanonische Eigenschaft)](pidtagruleactions-canonical-property.md)
  
[PidTagRuleProvider (kanonische Eigenschaft)](pidtagruleprovider-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

