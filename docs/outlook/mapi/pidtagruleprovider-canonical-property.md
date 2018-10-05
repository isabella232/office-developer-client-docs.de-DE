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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385977"
---
# <a name="pidtagruleprovider-canonical-property"></a>PidTagRuleProvider (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen der Anwendung, die eine Regel festlegt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W  <br/> |
|Kennung:  <br/> |0x6681  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Zurückgestellt Aktionen müssen diese Eigenschaften zum Identifizieren des Codes, die interpretiert werden und die Regelaktion ausführen müssen.
  
Regeln für Postfächer und Ordner gespeichert sind zugeordnet, mit der Anwendung, die sie von einer Regel Anbieterzeichenfolge besitzt. Ein Anbieter Regel festgelegt und Regeln in einer Regeltabelle behandelt. Es bietet auch eine Möglichkeit, alle zurückgestellten Aktionen verarbeiten, wenn solche Regeln festgelegt sind. Zurückgestellte Aktionen werden von den Informationsspeicher implizit erstellt. Für Vorgänge verschieben oder Kopieren auf einen anderen Wenn ein Anbieter in der Regel verzögerter Aktion Legt fest, muss es einen Ereignishandler bereitstellen, um die Aktion ausführen, wenn die Regel ausgelöst wird, und eine verzögerte Aktion erstellt wird.
  
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

