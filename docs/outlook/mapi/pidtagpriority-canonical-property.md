---
title: Kanonische Pidtagpriority (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339431"
---
# <a name="pidtagpriority-canonical-property"></a>Kanonische Pidtagpriority (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die relative Priorität einer Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PRIORITY  <br/> |
|Kennung:  <br/> |0x0026  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft und die **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))-Eigenschaft sollten nicht verwechselt werden. Wichtigkeit gibt einen Wert für Benutzer an, während Priority die Reihenfolge oder Geschwindigkeit angibt, mit der die Nachricht von der Messagingsystem Software gesendet werden soll. Höhere Priorität weist in der Regel auf höhere Kosten hin. Höhere Wichtigkeit wird in der Regel einer anderen Anzeige von der Benutzeroberfläche zugeordnet.
  
Die Priorität einer Berichtnachricht sollte mit der Priorität der gemeldeten ursprünglichen Nachricht übereinstimmen.
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
PRIO_NONURGENT 
  
> Die Nachricht ist nicht dringlich.
    
PRIO_NORMAL 
  
> Die Nachricht hat die normale Priorität.
    
PRIO_URGENT 
  
> Die Nachricht ist dringend.
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

