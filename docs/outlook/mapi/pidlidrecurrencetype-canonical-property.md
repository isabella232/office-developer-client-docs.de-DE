---
title: PidLidRecurrenceType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9fecd67c370333064fd593634ad2a924a3005d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793725"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>PidLidRecurrenceType (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt den Serientyp von sich wiederholenden Reihe.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidRecurType  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008231  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt an, welche Serie von sich wiederholenden Reihe mithilfe der unten aufgeführten Werte.
  
|**Status**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |Eine einzelne Instanz eines Termins.  <br/> |
|rectypeDaily  <br/> |1  <br/> |Ein tägliches Serienmuster.  <br/> |
|rectypeWeekly  <br/> |2  <br/> |Ein wöchentliches Serienmuster.  <br/> |
|rectypeMonthly  <br/> |3  <br/> |Ein monatliches Serienmuster.  <br/> |
|rectypeYearly  <br/> |4  <br/> |Ein jährliches Serienmuster.  <br/> |
   
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

