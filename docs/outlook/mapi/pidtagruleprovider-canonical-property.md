---
title: PidTagRuleProvider (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32a0e900c959b17dd7b1e61bdaa9c80a6f5d4966
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591479"
---
# <a name="pidtagruleprovider-canonical-property"></a>PidTagRuleProvider (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen der Anwendung, die eine Regel festlegt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W  <br/> |
|Kennung:  <br/> |0x6681  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verzögerte Aktionen benötigen diese Eigenschaften, um den Code zu identifizieren, der die Regelaktion interpretieren und ausführen muss.
  
Regeln, die in Postfächern und Ordnern gespeichert sind, sind der Anwendung zugeordnet, die sie durch eine Regelanbieterzeichenfolge besitzt. Ein Regelanbieter legt Regeln in einer Regeltabelle fest und behandelt sie. Es bietet auch eine Möglichkeit, verzögerte Aktionen zu behandeln, wenn solche Regeln festgelegt sind. Verzögerte Aktionen werden implizit vom Informationsspeicher erstellt. Wenn ein Anbieter eine Regel für verzögerte Aktionen festlegt, muss er für Verschiebungs- oder Kopiervorgänge in einen anderen Speicher einen Handler zum Ausführen der Aktion bereitstellen, wenn die Regel ausgelöst und eine verzögerte Aktion erstellt wird.
  
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

