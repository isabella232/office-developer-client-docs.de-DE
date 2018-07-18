---
title: Informationen zur Persistenz von TZDEFINITION für einen Stream, um ein Commit zu einer binären Eigenschaft durchzuführen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Die Eigenschaften der Zeitzone, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur und PidLidAppointmentTimeZoneDefinitionStartDisplay sind binär benannte Eigenschaften, von denen jedes enthält einen Datenstrom, der zugeordnet ist die beibehaltenen Format einer TZDEFINITION Struktur.
ms.openlocfilehash: 8e00c7203e2a0adfdf9ff3e6dadff6485c8b5111
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790917"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Informationen zur Persistenz von TZDEFINITION für einen Stream, um ein Commit zu einer binären Eigenschaft durchzuführen

Die Eigenschaften der Zeitzone, [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)und [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) sind binäre benannte Eigenschaften, von denen jedes enthält einen Datenstrom, der die beibehaltenen Format einer [TZDEFINITION](tzdefinition.md) Struktur zugeordnet ist. 
  
In diesem Thema wird ein little-endian-Format, die auf eine der drei binäre Eigenschaften commit für beim Speichern von **TZDEFINITION** in ein Stream-Objekt verwendet werden kann. Verwenden Sie das gleiche endian-Format in ein Parser interpretiert einen Streamwert, der von einem der folgenden Eigenschaften abgerufen werden. 
  
```cpp
BYTE  bMajorVersion;    // breaking change
BYTE  bMinorVersion;    // extensibility
WORD  cbHeader;         // size of following data until TZREG sub structure
WORD  wFlags;
if (TZDEFINITION_FLAG_VALID_GUID)
   GUID  guid;                // guid
if (TZDEFINITION_FLAG_VALID_KEYNAME)     
    WORD   cchKeyName;        // does not include null char
    WCHAR  rgchKeyName;       // not null terminated
    WORD  cRules;             // number of rules
// for each rule
   BYTE        bMajorVersion;         // breaking change
   BYTE        bMinorVersion;         // extensibility
   WORD        cbRule;                // size of following data
   WORD        wFlags;                // flags
   SYSTEMTIME  stStart;               // GMT when this rule starts
// Following are the fields of the TZREG sub structure
   long        lBias;                // offset from GMT
   long        lStandardBias;        // offset from bias during standard time
   long        lDaylightBias;        // offset from bias during daylight time
   SYSTEMTIME  stStandardDate;       // time to switch to standard time
   SYSTEMTIME  stDaylightDate;       // time to switch to daylight time
```

Die Nummer der Hauptversion wird verwendet, um stellen eine wichtige ändern. Clients, die mit die Hauptversionsnummer nicht vertraut sind, sollten die-Eigenschaft behandeln, sofern er nicht vorhanden ist. Schreiben die Struktur Clients sollten die Konstante **TZ_BIN_VERSION_MAJOR**angeben. 
  
Die Nummer der Nebenversion wird für die Erweiterbarkeit verwendet. Clients, die mit der Nummer der Nebenversion nicht vertraut sind, sollten die Daten lesen, die sie verstehen, und überspringen die Daten, die jeder Regel oder in der gesamten Stream-Objekt angefügt werden soll möglicherweise. Schreiben die Struktur Clients sollten die Konstante **TZ_BIN_VERSION_MINOR**angeben. 
  
Wenn ein Parser nicht die Hauptversion der Kopfzeile verstehen, muss Sie nicht den Rest der Struktur lesen und Verhalten, als ob die Daten nicht vorhanden ist. Wenn ein Parser nicht die Nebenversion der Kopfzeile verstehen, sollte **CbHeader** verwenden, um die Teile, die nicht erkannt und Advance, die Teile des Stream-Objekts lesen, die es versteht ignorieren. 
  
Der Wert der **wFlags** ist immer **TZDEFINITION_FLAG_VALID_KEYNAME**. Der Name des Schlüssels weist eine maximale Größe von **MAX_PATH**. 
  
Wenn ein Parser die Hauptversion einer Regel nicht erkannt wird, sollte der Client die Regel ignoriert und **CbRule** verwenden, um die Regel der nächsten zu wechseln. Wenn ein Parser die Nebenversion einer Regel nicht erkannt wird, sollte der Client nur die Teile der Regel analysieren, die es versteht. 
  
Wenn eine **TZDEFINITION** -Struktur in einem Stream-Objekt gespeichert, sollten ein Parser keine Informationen zu schreiben, die nicht erkannt werden. 
  
Die maximale Anzahl von Regeln lautet 1024.
  
Beachten Sie, dass die Struktur [TZREG](tzreg.md) hier anders beibehalten wird, als wenn alleine beibehalten, also desselben Codes verwendet werden kann, es zu analysieren. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)

