---
title: Kanonische PidLidTaskOrdinal-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 033bc038988373b11f3eac863a256717624999f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793848"
---
# <a name="pidlidtaskordinal-canonical-property"></a>Kanonische PidLidTaskOrdinal-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Bietet Hilfe benutzerdefinierten Sortierung Aufgaben.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTaskOrdinal  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008123  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann nicht festgelegt bleiben. Wenn festgelegt, dessen Wert größer als "0x800186A0" (-2,147,383,648) sein muss und weniger als "0x7FFE7960" (2,147,383,648) und unter Aufgaben im selben Ordner eindeutig sein müssen.
  
Wenn der Client diese Eigenschaft auf eine Zahl kleiner als den negativen Wert des aktuellen Werts der Eigenschaft **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) des Ordners festgelegt wird, muss der Client auch **PR_ORDINAL_MOST** für den Ordner aktualisieren. 
  
Die **PR_ORDINAL_MOST** -Eigenschaft des Ordners bietet eine effiziente Möglichkeit um einen eindeutigen Wert zwischen Aufgaben im selben Ordner zu bestimmen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert. 
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

