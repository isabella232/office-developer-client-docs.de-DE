---
title: Kanonische PidLidAppointmentTimeZoneDefinitionRecur-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5cff6ec7b39c26eec098d250688d98bf1e4799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793460"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Kanonische PidLidAppointmentTimeZoneDefinitionRecur-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen Datenstrom, der mit beibehaltenen Format einer Struktur [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) ist der die Beschreibung für die Zeitzone gespeichert, die verwendet wird, wenn eine Terminserie oder eine Besprechungsanfrage erstellt wird. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidApptTZDefRecur  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008260  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen basierend auf Collaboration Data Objects (CDO) 1.2.1 (engl.), die im Kalender von Outlook oder Exchange Server ausgeführt haben aktualisieren Tool verwendet die **DispidApptTZDefRecur** und ** DispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md))-Eigenschaften, um festzustellen, ob die Besprechungsserie angepasst werden soll, wenn die Regeln der Zeitzone ändern. Diese Eigenschaften müssen synchronisiert werden, weil ältere Clients die **DispidTimeZoneStruct** -Eigenschaft immer noch bearbeiten können. Um zu ermitteln, ob die beiden Eigenschaften synchronisiert werden, sollte der **wFlags** Member für die Regel, **die dispidtimezonestruct** entspricht, die TZRULE_FLAG_RECUR_CURRENT_TZREG gekennzeichnet sind. Wenn dieses Flag nicht festgelegt ist, oder es wird festgelegt, und die Regel in der **DispidTimeZoneStruct** -Eigenschaft nicht der markierten Regel entspricht, die **DispidApptTZDefRecur** -Eigenschaft verworfen werden muss und **DispidTimeZoneStruct** stattdessen verwendet werden soll. 
  
Beim Schreiben der **DispidApptTZDefRecur** und die **DispidTimeZoneStruct** -Eigenschaft um eine neue Besprechungsserie oder, wenn Sie eine beliebige Auswahl mit der **DispidTimeZoneStruct** -Eigenschaft, die aktuelle Definition für die Zeitzone (treffen gemäß die Windows-Registrierung) sollte verwendet werden. 
  
Ein Parser wird beim Lesen eines Stream-Objekts, das aus **DispidApptTZDefRecur**abgerufen wird, oder wenn er in ein Stream-Objekt für eine binäre Eigenschaft wie **DispidApptTZDefRecur**Engagement **TZDEFINITION** beibehalten. Weitere Informationen finden Sie unter [Speichern von TZDEFINITION in ein Stream-Objekt an eine binäre Eigenschaft übermittelt werden](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **DispidApptTZDefRecur** gibt die Informationen zur Zeitzone, die Beschreibung der Vorgehensweise die Besprechungsdatum und Uhrzeit auf einer Terminserie und von koordinierte Weltzeit (UTC) zu konvertieren. Wenn diese Eigenschaft wird festgelegt, aber es die Daten, die mit den Daten dargestellt durch **DispidTimeZoneStruct**inkonsistente hat, muss der Client **DispidTimeZoneStruct** anstelle von **DispidApptTZDefRecur**verwenden. Wenn **DispidApptTZDefRecur** nicht festgelegt ist, wird stattdessen die **PidLidTimeZoneStruct** -Eigenschaft verwendet werden. Die Felder in dieser BLOB werden in little-Endian-Bytereihenfolge codiert. 
  
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

