---
title: PidTagRuleProvider (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280605"
---
# <a name="pidtagruleprovider-canonical-property"></a>PidTagRuleProvider (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen der Anwendung, die eine Regel legt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W  <br/> |
|Kennung:  <br/> |0x6681  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Verzögerte Aktionen benötigen diese Eigenschaften, um den Code zu identifizieren, der die Regelaktion interpretieren und ausführen muss.
  
Regeln, die in Postfächern und Ordnern gespeichert sind, werden der Anwendung zugeordnet, der sie durch eine Regelanbieterzeichenfolge gehören. Ein Regelanbieter legt Regeln in einer Regeltabelle fest und verarbeitet diese. Es bietet auch eine Möglichkeit, alle zurückgestellten Aktionen zu behandeln, wenn solche Regeln festgelegt sind. Verzögerte Aktionen werden implizit vom Informationsspeicher erstellt. Wenn ein Anbieter eine verzögerte Aktionsregel für Vorgänge in einen anderen Speicher verschiebt oder kopiert, muss er einen Handler zum Ausführen der Aktion bereitstellen, wenn die Regel ausgelöst wird und eine verzögerte Aktion erstellt wird.
  
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

