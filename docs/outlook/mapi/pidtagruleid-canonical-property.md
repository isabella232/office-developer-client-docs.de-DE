---
title: Kanonische Pidtagruleid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359493"
---
# <a name="pidtagruleid-canonical-property"></a>Kanonische Pidtagruleid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen eindeutigen Bezeichner an, den der Messaging Server für jede Regel generiert, wenn die Regel erstellt wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_ID  <br/> |
|Kennung:  <br/> |0x6674  <br/> |
|Datentyp:  <br/> |PT_I8  <br/> |
|Bereich:  <br/> |Server seitige Regeln  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Client darf diese Eigenschaft beim Erstellen einer neuen Regel nicht angeben, muss diese jedoch beim Ändern oder Löschen einer Regel angeben.
  
Beim Löschen einer Regel ist die einzige Eigenschaft, die der Client passieren muss, **PR_RULE_ID** und sollte keine andere Eigenschaft aufweisen. Der Server muss andere Eigenschaften als diese Eigenschaft ignorieren. Beim Hinzufügen einer Regel darf der Client nicht in **PR_RULE_ID**passieren, er muss die **PR_RULE_CONDITION** ([pidtagrulecondition (](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) und **PR_RULE_PROVIDER** ([ Pidtagruleprovider (](pidtagruleprovider-canonical-property.md))-Eigenschaften. Beim Ändern einer Regel muss der Client **PR_RULE_ID** passieren und die restlichen Eigenschaften, die geändert werden müssen, weitergeben. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Bearbeitet eingehende e-Mail-Nachrichten auf einem Server.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagrulecondition (-Eigenschaft](pidtagrulecondition-canonical-property.md)
  
[Kanonische PidTagRuleActions-Eigenschaft](pidtagruleactions-canonical-property.md)
  
[Kanonische Pidtagruleprovider (-Eigenschaft](pidtagruleprovider-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

