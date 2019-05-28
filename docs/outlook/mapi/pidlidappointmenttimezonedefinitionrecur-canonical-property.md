---
title: Kanonische pidlidappointmenttimezonedefinitionrecur (-Eigenschaft
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
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Kanonische pidlidappointmenttimezonedefinitionrecur (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Datenstrom, der dem beibehaltenen Format einer [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) -Struktur zugeordnet wird, in der die Beschreibung für die Zeitzone gespeichert wird, die beim Erstellen einer Terminserie oder Besprechungsanfrage verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptTZDefRecur  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x00008260  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen basierend auf Collaboration Data Objects (CDO) 1.2.1, die das Outlook-oder Exchange Server-Kalender Update Tool ausgeführt haben, verwenden die **dispidApptTZDefRecur** und ** dispidTimeZoneStruct** ([pidlidtimezonestruct (](pidlidtimezonestruct-canonical-property.md))-Eigenschaften, um zu bestimmen, ob die Besprechungsserie angepasst werden soll, wenn sich die Regeln der Zeitzone ändern. Diese Eigenschaften müssen synchronisiert werden, da ältere Clients die **dispidTimeZoneStruct** -Eigenschaft möglicherweise noch bearbeiten. Um zu ermitteln, ob die beiden Eigenschaften synchronisiert werden, sollte das **wFlags** -Element für die Regel, die mit **dispidTimeZoneStruct** übereinstimmt, das TZRULE_FLAG_RECUR_CURRENT_TZREG-Flag festgelegt haben. Wenn dieses Flag nicht festgelegt oder festgelegt ist und die Regel in der **dispidTimeZoneStruct** -Eigenschaft nicht mit der markierten Regel übereinstimmt, sollte die **dispidApptTZDefRecur** -Eigenschaft verworfen und stattdessen **dispidTimeZoneStruct** verwendet werden. 
  
Wenn Sie die **dispidApptTZDefRecur** -und **dispidTimeZoneStruct** -Eigenschaften in eine neue Besprechungsserie schreiben oder wenn Sie eine beliebige Auswahl treffen, um die **dispidTimeZoneStruct** -Eigenschaft zu verwenden, wird die aktuelle Definition für die Zeitzone ( entsprechend der Windows-Registrierung) sollte verwendet werden. 
  
Ein Parser muss vorsichtig sein, wenn er einen Datenstrom liest, der von **dispidApptTZDefRecur**abgerufen wird, oder wenn er **TZDEFINITION** in einem Stream zur Bindung an eine binäre Eigenschaft wie **dispidApptTZDefRecur**speichert. Weitere Informationen finden Sie unter [about persistent TZDEFINITION to a Stream to Commit to a binary Property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** gibt Zeitzoneninformationen an, in denen beschrieben wird, wie das Besprechungsdatum und die Uhrzeit in einer wiederkehrenden Reihe in und aus der koordinierten Weltzeit (Coordinated Universal Time, UTC) konvertiert werden. Wenn diese Eigenschaft festgelegt ist, aber Daten enthält, die nicht mit den von **dispidTimeZoneStruct**dargestellten Daten übereinstimmen, muss der Client **dispidTimeZoneStruct** anstelle von **dispidApptTZDefRecur**verwenden. Wenn **dispidApptTZDefRecur** nicht festgelegt ist, wird stattdessen die **pidlidtimezonestruct (** -Eigenschaft verwendet. Die Felder in diesem BLOB werden in Little-Endian-Bytereihenfolge codiert. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

