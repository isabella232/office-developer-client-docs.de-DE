---
title: Informationen zur Persistenz von TZDEFINITION für einen Stream, um ein Commit zu einer binären Eigenschaft durchzuführen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Die Zeitzoneneigenschaften Pidlidappointmenttimezonedefinitionenddisplay (, Pidlidappointmenttimezonedefinitionrecur (und Pidlidappointmenttimezonedefinitionstartdisplay (sind binäre benannte Eigenschaften, die jeweils einen Stream enthalten, der dem dauerhaftes Format einer TZDEFINITION-Struktur.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316975"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Informationen zur Persistenz von TZDEFINITION für einen Stream, um ein Commit zu einer binären Eigenschaft durchzuführen

Die Zeitzoneneigenschaften [pidlidappointmenttimezonedefinitionenddisplay (](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [pidlidappointmenttimezonedefinitionrecur (](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)und [pidlidappointmenttimezonedefinitionstartdisplay (](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) sind binäre benannte Eigenschaften, die jeweils enthält einen Stream, der dem beibehaltenen Format einer [TZDEFINITION](tzdefinition.md) -Struktur zugeordnet ist. 
  
In diesem Thema wird ein kleines Endian-Format beschrieben, das beim Speichern von **TZDEFINITION** in einem Stream verwendet werden kann, um eine der drei binären Eigenschaften zu übernehmen. Verwenden Sie das gleiche Endian-Format in einem Parser, um einen Datenstromwert zu interpretieren, der von einer dieser Eigenschaften abgerufen wurde. 
  
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

Die Hauptversionsnummer wird verwendet, um eine unterbrechende Änderung vorzunehmen. Clients, die mit der Hauptversionsnummer nicht vertraut sind, sollten die Eigenschaft so behandeln, als ob Sie nicht vorhanden ist. Clients, die die Struktur schreiben, sollten die Konstante **TZ_BIN_VERSION_MAJOR**angeben. 
  
Die Nebenversionsnummer wird zur Erweiterbarkeit verwendet. Clients, die mit der Nebenversionsnummer nicht vertraut sind, sollten die Daten lesen, die Sie verstehen, und die Daten überspringen, die möglicherweise jeder Regel oder dem Gesamtdaten Strom angefügt werden. Clients, die die Struktur schreiben, sollten die Konstante **TZ_BIN_VERSION_MINOR**angeben. 
  
Wenn ein Parser die Hauptversion der Kopfzeile nicht versteht, sollte er nicht den Rest der Struktur lesen und sich Verhalten, als ob die Daten fehlen. Wenn ein Parser die Nebenversion des Headers nicht versteht, sollte er **cbHeader** verwenden, um die Teile zu ignorieren, die er nicht versteht, und um die Teile des Streams zu lesen, die er versteht. 
  
Der Wert von **wFlags** ist immer **TZDEFINITION_FLAG_VALID_KEYNAME**. Der Schlüsselname hat eine maximale Größe von **MAX_PATH**. 
  
Wenn ein Parser die Hauptversion einer Regel nicht erkennt, sollte der Client die Regel ignorieren und **cbRule** verwenden, um zur nächsten Regel zu wechseln. Wenn ein Parser die Nebenversion einer Regel nicht erkennt, sollte der Client nur die Teile der Regel analysieren, die er versteht. 
  
Wenn Sie eine **TZDEFINITION** -Struktur in einem Stream beibehalten, sollte ein Parser nicht versuchen, Informationen zu schreiben, die er nicht versteht. 
  
Die maximale Anzahl von Regeln ist 1024.
  
Beachten Sie, dass die [TZREG](tzreg.md) -Struktur hier unterschiedlich gespeichert wird, als bei Beibehaltung allein, sodass derselbe Code nicht zum Analysieren verwendet werden kann. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)

