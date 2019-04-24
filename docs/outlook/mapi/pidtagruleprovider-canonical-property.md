---
title: Kanonische Pidtagruleprovider (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280605"
---
# <a name="pidtagruleprovider-canonical-property"></a>Kanonische Pidtagruleprovider (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen der Anwendung, die eine Regel festlegt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W  <br/> |
|Kennung:  <br/> |0x6681  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Server seitige Regeln  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verzögerte Aktionen benötigen diese Eigenschaften, um den Code zu identifizieren, der die Regelaktion interpretieren und ausführen muss.
  
Regeln, die in Postfächern und Ordnern gespeichert sind, sind der Anwendung zugeordnet, die Sie durch eine Zeichenfolge des Regel Anbieters besitzt. Ein Regel Anbieter legt Regeln in einer Regeltabelle fest und verarbeitet sie. Sie bietet auch eine Möglichkeit, verzögerte Aktionen zu behandeln, wenn solche Regeln festgelegt werden. Verzögerte Aktionen werden implizit vom Informationsspeicher erstellt. Bei Verschiebungs-oder Kopiervorgängen in einen anderen Speicher muss ein Anbieter, der eine verzögerte Aktionsregel festlegt, einen Handler bereitstellen, um die Aktion auszuführen, wenn die Regel ausgelöst wird und eine verzögerte Aktion erstellt wird.
  
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

