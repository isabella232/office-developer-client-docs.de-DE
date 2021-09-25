---
title: Informationen zur Persistenz von TZDEFINITION für einen Stream, um ein Commit zu einer binären Eigenschaft durchzuführen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Die Zeitzoneneigenschaften PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur und PidLidAppointmentTimeZoneDefinitionStartDisplay sind binäre benannte Eigenschaften, die jeweils einen Datenstrom enthalten, der dem dauerhaften Format einer TZDEFINITION-Struktur zugeordnet ist.
ms.openlocfilehash: 6925068faf9e4e4e700ea8d2aae2fd25dc98cdb1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592837"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Informationen zur Persistenz von TZDEFINITION für einen Stream, um ein Commit zu einer binären Eigenschaft durchzuführen

Die Zeitzoneneigenschaften [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)und [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) sind binäre benannte Eigenschaften, die jeweils einen Datenstrom enthalten, der dem beibehaltenen Format einer [TZDEFINITION-Struktur](tzdefinition.md) zugeordnet ist. 
  
In diesem Thema wird ein kleines endisches Format beschrieben, das verwendet werden kann, wenn **TZDEFINITION** in einem Stream gespeichert wird, um einen Commit für eine von drei binären Eigenschaften auszuführen. Verwenden Sie dasselbe Endianformat in einem Parser, um einen Datenstromwert zu interpretieren, der von einer dieser Eigenschaften abgerufen wird. 
  
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

Die Hauptversionsnummer wird verwendet, um eine grundlegende Änderung vorzunehmen. Clients, die mit der Hauptversionsnummer nicht vertraut sind, sollten die Eigenschaft so behandeln, als wäre sie nicht vorhanden. Clients, die die Struktur schreiben, sollten die Konstante **TZ_BIN_VERSION_MAJOR** angeben. 
  
Die Nebenversionsnummer wird zur Erweiterbarkeit verwendet. Clients, die mit der Nebenversionsnummer nicht vertraut sind, sollten die ihnen verständlichen Daten lesen und die Daten überspringen, die möglicherweise an jede Regel oder an den gesamten Datenstrom angefügt werden. Clients, die die Struktur schreiben, sollten die Konstante **TZ_BIN_VERSION_MINOR** angeben. 
  
Wenn ein Parser die Hauptversion des Headers nicht versteht, sollte er den Rest der Struktur nicht lesen und sich so verhalten, als ob die Daten fehlen. Wenn ein Parser die Nebenversion des Headers nicht versteht, sollte er **cbHeader** verwenden, um die Teile zu ignorieren, die er nicht versteht, und die Teile des Datenstroms, den er versteht, zu lesen. 
  
Der Wert von **wFlags** ist immer **TZDEFINITION_FLAG_VALID_KEYNAME.** Der Schlüsselname hat eine maximale Größe von **MAX_PATH.** 
  
Wenn ein Parser die Hauptversion einer Regel nicht erkennt, sollte der Client die Regel ignorieren und **cbRule** verwenden, um zur nächsten Regel übergehen zu können. Wenn ein Parser die Nebenversion einer Regel nicht erkennt, sollte der Client nur die Teile der Regel analysieren, die er versteht. 
  
Wenn eine **TZDEFINITION-Struktur** in einem Stream gespeichert wird, sollte ein Parser nicht versuchen, Informationen zu schreiben, die er nicht versteht. 
  
Die maximale Anzahl von Regeln beträgt 1024.
  
Beachten Sie, dass die [TZREG-Struktur](tzreg.md) hier anders beibehalten wird als wenn sie allein beibehalten wird, sodass derselbe Code nicht zum Analysieren verwendet werden kann. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)

