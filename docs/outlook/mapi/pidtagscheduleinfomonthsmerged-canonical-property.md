---
title: PidTagScheduleInfoMonthsMerged (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c1096df0eff4b43239978620f4ccf2e9d221095a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795108"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>PidTagScheduleInfoMonthsMerged (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Liste der, die Monate, für welche Frei/Gebucht-Daten vom Typ beschäftigt oder einen außerhalb von Office (OOF) Nachricht in der Frei/Gebucht-Nachricht vorhanden ist. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|Bezeichner:  <br/> |0x684F  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Frei/Gebucht-Informationen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ereignisse vom Typ mit Vorbehalt Frei/Gebucht-Informationen sind nicht in dieser Eigenschaft enthalten. Die Syntax der-Format und Integritätsregeln dieser Eigenschaft werden die gleichen, die von **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), aber finden Sie unter Termine, die auf das zugehörige Calendar-Objekt ABWESEND oder beschäftigt gekennzeichnet sind. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.
    
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

