---
title: Informationen zur Persistenz von TZDEFINITION für einen Stream, um ein Commit zu einer binären Eigenschaft durchzuführen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Die Zeitzoneneigenschaften PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur und PidLidAppointmentTimeZoneDefinitionStartDisplay sind binär benannte Eigenschaften, die jeweils einen Datenstrom enthalten, der dem dauerhaften Format einer TZDEFINITION-Struktur zu ordnet.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316975"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="a28ae-103">Informationen zur Persistenz von TZDEFINITION für einen Stream, um ein Commit zu einer binären Eigenschaft durchzuführen</span><span class="sxs-lookup"><span data-stu-id="a28ae-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="a28ae-104">Die Zeitzoneneigenschaften [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)und [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) sind binär benannte Eigenschaften, die jeweils einen Datenstrom enthalten, der dem dauerhaften Format einer [TZDEFINITION-Struktur](tzdefinition.md) zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="a28ae-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="a28ae-105">In diesem Thema wird ein kleines Endianformat beschrieben, das verwendet werden kann, wenn **TZDEFINITION** für einen Datenstrom beibehalten wird, um einen Commit für eine von drei binären Eigenschaften zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a28ae-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="a28ae-106">Verwenden Sie dasselbe Endianformat in einem Parser, um einen Datenstromwert zu interpretieren, der aus einer dieser Eigenschaften ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a28ae-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
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

<span data-ttu-id="a28ae-107">Die Hauptversionsnummer wird verwendet, um eine wichtige Änderung vor sich zu nehmen.</span><span class="sxs-lookup"><span data-stu-id="a28ae-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="a28ae-108">Clients, die mit der Hauptversionsnummer nicht vertraut sind, sollten die Eigenschaft so behandeln, als wäre sie nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a28ae-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="a28ae-109">Clients, die die Struktur schreiben, sollten die Konstante **TZ_BIN_VERSION_MAJOR.**</span><span class="sxs-lookup"><span data-stu-id="a28ae-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="a28ae-110">Die Nebenversionsnummer wird für die Erweiterbarkeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="a28ae-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="a28ae-111">Clients, die mit der Nebenversionsnummer nicht vertraut sind, sollten die daten lesen, die sie verstehen, und die Daten überspringen, die möglicherweise an jede Regel oder an den gesamten Datenstrom angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a28ae-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="a28ae-112">Clients, die die Struktur schreiben, sollten die Konstante **TZ_BIN_VERSION_MINOR.**</span><span class="sxs-lookup"><span data-stu-id="a28ae-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="a28ae-113">Wenn ein Parser die Hauptversion des Headers nicht versteht, sollte er den Rest der Struktur nicht lesen und sich so verhalten, als würden die Daten fehlen.</span><span class="sxs-lookup"><span data-stu-id="a28ae-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="a28ae-114">Wenn ein Parser die Nebenversion des Headers nicht versteht, sollte er **cbHeader** verwenden, um die Teile zu ignorieren, die er nicht versteht, und die Teile des Datenstroms zu lesen, die er versteht.</span><span class="sxs-lookup"><span data-stu-id="a28ae-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="a28ae-115">Der Wert von **wFlags** ist immer **TZDEFINITION_FLAG_VALID_KEYNAME.**</span><span class="sxs-lookup"><span data-stu-id="a28ae-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="a28ae-116">Der Schlüsselname hat eine maximale Größe von **MAX_PATH**.</span><span class="sxs-lookup"><span data-stu-id="a28ae-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="a28ae-117">Wenn ein Parser die Hauptversion einer Regel nicht erkennt, sollte der Client die Regel ignorieren und **cbRule** verwenden, um zur nächsten Regel vorzusprungen.</span><span class="sxs-lookup"><span data-stu-id="a28ae-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="a28ae-118">Wenn ein Parser die Nebenversion einer Regel nicht erkennt, sollte der Client nur die Teile der Regel analysieren, die er versteht.</span><span class="sxs-lookup"><span data-stu-id="a28ae-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="a28ae-119">Wenn eine **TZDEFINITION-Struktur** in einem Datenstrom beibehalten wird, sollte ein Parser nicht versuchen, Informationen zu schreiben, die er nicht versteht.</span><span class="sxs-lookup"><span data-stu-id="a28ae-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="a28ae-120">Die maximale Anzahl von Regeln ist 1024.</span><span class="sxs-lookup"><span data-stu-id="a28ae-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="a28ae-121">Beachten Sie, [dass die TZREG-Struktur](tzreg.md) hier anders beibehalten wird, als wenn sie allein beibehalten wird, sodass nicht derselbe Code verwendet werden kann, um sie zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="a28ae-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a28ae-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a28ae-122">See also</span></span>

- [<span data-ttu-id="a28ae-123">Konstanten (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="a28ae-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="a28ae-124">Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur</span><span class="sxs-lookup"><span data-stu-id="a28ae-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="a28ae-125">Lesen von Zeitzoneneigenschaften aus einem Termin</span><span class="sxs-lookup"><span data-stu-id="a28ae-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

