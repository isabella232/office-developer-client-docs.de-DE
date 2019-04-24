---
title: Kanonische PidTagRuleActions-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278900"
---
# <a name="pidtagruleactions-canonical-property"></a>Kanonische PidTagRuleActions-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die mit der Regel verknüpften Aktionen. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_ACTIONS  <br/> |
|Kennung:  <br/> |0x6680  <br/> |
|Datentyp:  <br/> |PT_ACTIONS  <br/> |
|Bereich:  <br/> |Server seitige Regeln  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Aktionen werden als Regelaktion ausgedrückt, und der Wert Puffer der Eigenschaft enthält die in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)verpackte Datenpuffer Struktur für Regelaktionen.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ImportProcs. cpp  <br/> |PropCopyMore, HrCopyActions  <br/> |Diese Funktionen veranschaulichen, wie Sie eine PT_ACTIONS-Eigenschaft zum Kopieren in eine andere Eigenschaft analysieren.  <br/> |
   
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

