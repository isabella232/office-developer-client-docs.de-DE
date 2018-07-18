---
title: PidLidIsException (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5a36cf21a36f83ec252923ddbb137b3b99456927
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793634"
---
# <a name="pidlidisexception-canonical-property"></a>PidLidIsException (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt an, dass das Objekt, das eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |LID_IS_EXCEPTION  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Meeting  <br/> |
|Long-ID (Abdeckung):  <br/> |0x0000000A  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Gibt der Wert FALSE an, dass das Objekt, das eine Terminserie oder eine einzelne Instanz darstellt. Das Fehlen dieser Eigenschaft für jedes Objekt gilt gibt einen Wert false mit Ausnahme der Ausnahme eingebettete Nachricht, die Wert TRUE wird davon ausgegangen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

