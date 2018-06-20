---
title: Kanonische-Eigenschaft PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794475"
---
# <a name="pidtagimportance-canonical-property"></a>Kanonische-Eigenschaft PidTagImportance

  
  
**Betrifft**: Outlook 
  
Enthält einen Wert, der den Nachrichtenabsender Opinion die Wichtigkeitsstufe einer Nachricht angibt. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_IMPORTANCE  <br/> |
|Bezeichner:  <br/> |0x0017  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft und die **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))-Eigenschaft darf nicht verwechselt werden. Bedeutung der Wert für Benutzer, während der Priorität angibt, die Reihenfolge oder Geschwindigkeit, an dem die Nachricht soll, von der messaging-Systemsoftware gesendet werden, an. Höherer Priorität Gibt in der Regel höhere Kosten. Höhere Priorität ist in der Regel eine andere Darstellung von der Benutzeroberfläche zugeordnet. 
  
Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
  
IMPORTANCE_LOW 
  
> Die Nachricht weist Wichtigkeit ' Niedrig '.
    
IMPORTANCE_HIGH 
  
> Die Nachricht weist hohen Priorität.
    
IMPORTANCE_NORMAL 
  
> Die Nachricht weist die normale Bedeutung.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
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

