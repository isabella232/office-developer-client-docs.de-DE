---
title: Zelle "Type" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Gibt einen Datentyp für den Textfeldwert an.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358926"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="20eac-103">Zelle "Type" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="20eac-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="20eac-104">Gibt einen Datentyp für den Textfeldwert an.</span><span class="sxs-lookup"><span data-stu-id="20eac-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="20eac-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="20eac-105">**Value**</span></span>|<span data-ttu-id="20eac-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20eac-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20eac-107">0</span><span class="sxs-lookup"><span data-stu-id="20eac-107">0</span></span>  <br/> |<span data-ttu-id="20eac-108">Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="20eac-108">String.</span></span>  <br/> |
|<span data-ttu-id="20eac-109">2</span><span class="sxs-lookup"><span data-stu-id="20eac-109">2</span></span>  <br/> |<span data-ttu-id="20eac-p101">Number. Enthält Datum, Uhrzeit, Zeitdauer, Währungs- und Skalarwerte sowie Maß- und Winkelangaben. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="20eac-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="20eac-113">5</span><span class="sxs-lookup"><span data-stu-id="20eac-113">5</span></span>  <br/> |<span data-ttu-id="20eac-p102">Datums- oder Uhrzeitwert. Zeigt Tage, Monate und Jahre oder Sekunden, Minuten und Stunden bzw. einen gemischten Datums- und Uhrzeitwert an. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="20eac-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="20eac-117">6</span><span class="sxs-lookup"><span data-stu-id="20eac-117">6</span></span>  <br/> |<span data-ttu-id="20eac-p103">Zeitdauerwert. Zeigt die verstrichene Zeit an. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="20eac-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="20eac-121">7</span><span class="sxs-lookup"><span data-stu-id="20eac-121">7</span></span>  <br/> |<span data-ttu-id="20eac-p104">Währungswert. Verwendet die aktuelle Landes-/Regionaleinstellungen des Systems. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="20eac-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20eac-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20eac-125">Remarks</span></span>

<span data-ttu-id="20eac-126">Sie können den Wert dieser Zelle auch über das Dialogfeld **Feld** festlegen (wenn ein Shape ausgewählt ist, klicken Sie auf der Registerkarte **Einfügen** in der Gruppe **Text** auf **Feld** ).</span><span class="sxs-lookup"><span data-stu-id="20eac-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="20eac-127">Wenn Sie einen Verweis auf die Zelle "Type" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="20eac-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20eac-128">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="20eac-128">Cell name:</span></span>  <br/> |<span data-ttu-id="20eac-129">Fields. Type [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="20eac-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="20eac-130">Wenn Sie einen Verweis auf die Zelle Type nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="20eac-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20eac-131">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="20eac-131">Section index:</span></span>  <br/> |<span data-ttu-id="20eac-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="20eac-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="20eac-133">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="20eac-133">Row index:</span></span>  <br/> |<span data-ttu-id="20eac-134">**visRowField** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="20eac-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="20eac-135">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="20eac-135">Cell index:</span></span>  <br/> |<span data-ttu-id="20eac-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="20eac-136">**visFieldType**</span></span> <br/> |
   

