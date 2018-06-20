---
title: Kanonische PidTagOriginalSensitivity-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6d461c88e96a3f749595b3e071737107480472aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794722"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a>Kanonische PidTagOriginalSensitivity-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die vom Absender der ersten Version einer Nachricht zugewiesen Vertraulichkeitsstufe d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ORIGINAL_SENSITIVITY  <br/> |
|Bezeichner:  <br/> |0x002E  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Clientanwendung sollte diese Eigenschaft auf denselben Wert festgelegt wie die **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))-Eigenschaft, wenn die Nachricht wird gesendet. Es sollte niemals später geändert werden.
  
Diese Eigenschaft wird von der Adressbuchhierarchie verwendet, um die Vertraulichkeit auf kopierten Einträge zu schützen. Sie können sie beispielsweise zum Blockieren der Änderung von der Text der ursprünglichen Nachricht in einer Weiterleitung des oder der Antwort auf eine Nachricht, die ursprünglich **SENSITIVITY_PRIVATE**gekennzeichnet wurde.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.
    
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

