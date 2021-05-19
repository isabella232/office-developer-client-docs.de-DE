---
title: PidLidAppointmentTimeZoneDefinitionRecur (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345353"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionRecur (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Datenstrom, der dem dauerhaften Format einer [TZDEFINITION-Struktur](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) zu ordnet, in der die Beschreibung für die Zeitzone gespeichert wird, die beim Erstellen eines Termins oder einer Besprechungsserie verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptTZDefRecur  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x00008260  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen, die auf den Eigenschaften Collaboration Data Objects (CDO) 1.2.1 basieren, die das Kalenderupdatetool Outlook oder Exchange Server ausgeführt haben, verwenden die **Eigenschaften dispidApptTZDefRecur** und **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), um zu bestimmen, ob die Besprechungsserie angepasst werden soll, wenn sich die Regeln der Zeitzone ändern. Diese Eigenschaften müssen synchronisiert werden, da ältere Clients möglicherweise weiterhin die **dispidTimeZoneStruct-Eigenschaft** bearbeiten. Um zu ermitteln, ob die beiden Eigenschaften synchronisiert sind, sollte das **wFlags-Element** für die Regel, die **dispidTimeZoneStruct** entspricht, über TZRULE_FLAG_RECUR_CURRENT_TZREG verfügen. Wenn dieses Flag nicht festgelegt oder festgelegt ist und die Regel in der **dispidTimeZoneStruct-Eigenschaft** nicht mit der markierten Regel übereinstimmen, sollte die **dispidApptTZDefRecur-Eigenschaft** verworfen und **stattdessen dispidTimeZoneStruct** verwendet werden. 
  
Wenn Sie die Eigenschaften **dispidApptTZDefRecur** und **dispidTimeZoneStruct** in eine neue Besprechungsserie schreiben, oder wenn Sie eine beliebige Entscheidung für die Verwendung der **dispidTimeZoneStruct-Eigenschaft** treffen, sollte die aktuelle Definition für die Zeitzone (gemäß der Windows-Registrierung) verwendet werden. 
  
Ein Parser muss vorsichtig sein, wenn er einen Datenstrom liest, der von **dispidApptTZDefRecur** erhalten wird, oder wenn **er TZDEFINITION** in einem Datenstrom für die Verpflichtung zu einer binären Eigenschaft wie **dispidApptTZDefRecur** beibehalten. Weitere Informationen finden Sie unter [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** gibt Zeitzoneninformationen an, die beschreiben, wie Das Datum und die Uhrzeit der Besprechung in einer Serie in koordinierte Weltzeit (Coordinated Universal Time, UTC) konvertiert werden. Wenn diese Eigenschaft festgelegt ist, aber Daten enthält, die mit den durch **dispidTimeZoneStruct** dargestellten Daten inkonsistent sind, muss der Client **dispidTimeZoneStruct** anstelle von **dispidApptTZDefRecur verwenden.** Wenn **dispidApptTZDefRecur** nicht festgelegt ist, wird stattdessen die **PidLidTimeZoneStruct-Eigenschaft** verwendet. Die Felder in diesem BLOB werden in klein-endischer Bytereihenfolge codiert. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

