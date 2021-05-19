---
title: PidTagRuleProviderData (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335420"
---
# <a name="pidtagruleproviderdata-canonical-property"></a>PidTagRuleProviderData (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine undurchsichtige Eigenschaft, die der Client für die ausschließliche Verwendung des Clients legt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_PROVIDER_DATA  <br/> |
|Kennung:  <br/> |0x6684  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Server muss den Wert dieser Eigenschaft beibehalten, wenn er vom Client festgelegt wurde, aber seinen Inhalt während der Regelauswertung und -verarbeitung ignorieren.
  
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
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind. 
    
## <a name="see-also"></a>Siehe auch



[PidTagRuleProvider (kanonische Eigenschaft)](pidtagruleprovider-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

