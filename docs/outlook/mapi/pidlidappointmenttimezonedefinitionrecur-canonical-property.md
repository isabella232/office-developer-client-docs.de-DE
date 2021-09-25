---
title: Kanonische PidLidAppointmentTimeZoneDefinitionRecur-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 83e72d3862ef38d93dace38b91e7a8a70ecb538c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583933"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Kanonische PidLidAppointmentTimeZoneDefinitionRecur-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Datenstrom, der dem beibehaltenen Format einer [TZDEFINITION-Struktur](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) zugeordnet ist, in dem die Beschreibung für die Zeitzone gespeichert wird, die beim Erstellen einer Terminserie oder Besprechungsanfrage verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptTZDefRecur  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008260  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen, die auf COLLABORATION Data Objects (CDO) 1.2.1 basieren und das Outlook- oder Exchange Server Kalenderaktualisierungstool ausgeführt haben, verwenden die Eigenschaften **dispidApptTZDefRecur** und **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) für bestimmen Sie, ob die Besprechungsserie angepasst werden soll, wenn sich die Regeln der Zeitzone ändern. Diese Eigenschaften müssen synchronisiert werden, da ältere Clients die **dispidTimeZoneStruct-Eigenschaft** möglicherweise noch bearbeiten. Um zu erkennen, ob die beiden Eigenschaften synchronisiert werden, sollte für das **wFlags-Element** für die Regel, die **dispidTimeZoneStruct entspricht,** das TZRULE_FLAG_RECUR_CURRENT_TZREG Flag festgelegt sein. Wenn dieses Flag nicht festgelegt ist oder festgelegt ist und die Regel in der **dispidTimeZoneStruct-Eigenschaft** nicht mit der markierten Regel übereinstimmt, sollte die **dispidApptTZDefRecur-Eigenschaft** verworfen und **stattdessen dispidTimeZoneStruct** verwendet werden. 
  
Wenn Sie die Eigenschaften **dispidApptTZDefRecur** und **dispidTimeZoneStruct** in eine neue Besprechungsserie schreiben oder wenn Sie eine beliebige Wahl zur Verwendung der **dispidTimeZoneStruct-Eigenschaft** treffen, sollte die aktuelle Definition für die Zeitzone (gemäß der Windows Registrierung) verwendet werden. 
  
Ein Parser muss vorsichtig sein, wenn er einen Stream liest, der aus **dispidApptTZDefRecur** abgerufen wird, oder wenn **TZDEFINITION** in einem Stream gespeichert wird, um eine binäre Eigenschaft wie **dispidApptTZDefRecur** zu verwenden. Weitere Informationen finden Sie unter [Informationen zum Beibehalten von TZDEFINITION in einem Stream, um einen Commit für eine binäre Eigenschaft auszuführen.](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)
  
 **dispidApptTZDefRecur** gibt Zeitzoneninformationen an, in denen beschrieben wird, wie Das Besprechungsdatum und die Besprechungszeit einer Terminserie in und aus koordinierter Weltzeit (UTC) konvertiert werden. Wenn diese Eigenschaft festgelegt ist, aber Daten enthält, die mit den durch **dispidTimeZoneStruct** dargestellten Daten inkonsistent sind, muss der Client **dispidTimeZoneStruct** anstelle von **dispidApptTZDefRecur** verwenden. Wenn **dispidApptTZDefRecur** nicht festgelegt ist, wird stattdessen die **PidLidTimeZoneStruct-Eigenschaft** verwendet. Die Felder in diesem BLOB werden in kleiner endischer Bytereihenfolge codiert. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

