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
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798328"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="0d71a-103">Type Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="0d71a-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="0d71a-104">Gibt einen Datentyp für den Textfeldwert an.</span><span class="sxs-lookup"><span data-stu-id="0d71a-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="0d71a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0d71a-105">**Value**</span></span>|<span data-ttu-id="0d71a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d71a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d71a-107">0</span><span class="sxs-lookup"><span data-stu-id="0d71a-107">0</span></span>  <br/> |<span data-ttu-id="0d71a-108">Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0d71a-108">String.</span></span>  <br/> |
|<span data-ttu-id="0d71a-109">2</span><span class="sxs-lookup"><span data-stu-id="0d71a-109">2</span></span>  <br/> |<span data-ttu-id="0d71a-p101">Number. Enthält Datum, Uhrzeit, Zeitdauer, Währungs- und Skalarwerte sowie Maß- und Winkelangaben. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="0d71a-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0d71a-113">5</span><span class="sxs-lookup"><span data-stu-id="0d71a-113">5</span></span>  <br/> |<span data-ttu-id="0d71a-p102">Datums- oder Uhrzeitwert. Zeigt Tage, Monate und Jahre oder Sekunden, Minuten und Stunden bzw. einen gemischten Datums- und Uhrzeitwert an. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="0d71a-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0d71a-117">6</span><span class="sxs-lookup"><span data-stu-id="0d71a-117">6</span></span>  <br/> |<span data-ttu-id="0d71a-p103">Zeitdauerwert. Zeigt die verstrichene Zeit an. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="0d71a-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0d71a-121">7</span><span class="sxs-lookup"><span data-stu-id="0d71a-121">7</span></span>  <br/> |<span data-ttu-id="0d71a-p104">Währungswert. Verwendet die aktuellen Landes-/Regionaleinstellungen des Systems. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="0d71a-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d71a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d71a-125">Remarks</span></span>

<span data-ttu-id="0d71a-126">Sie können auch den Wert dieser Zelle im Dialogfeld **Feld** festlegen (klicken Sie mit einem Shape ausgewählt haben, klicken Sie auf der Registerkarte **Einfügen** in der Gruppe **Text** auf **Feld** ).</span><span class="sxs-lookup"><span data-stu-id="0d71a-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="0d71a-127">Zum Abrufen eines Verweises auf die Zelle Type nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0d71a-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d71a-128">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0d71a-128">Cell name:</span></span>  <br/> |<span data-ttu-id="0d71a-129">Fields.Type [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0d71a-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0d71a-130">Wenn Sie einen Verweis auf die Zelle Type aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0d71a-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d71a-131">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0d71a-131">Section index:</span></span>  <br/> |<span data-ttu-id="0d71a-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="0d71a-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="0d71a-133">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0d71a-133">Row index:</span></span>  <br/> |<span data-ttu-id="0d71a-134">**VisRowField** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0d71a-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0d71a-135">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0d71a-135">Cell index:</span></span>  <br/> |<span data-ttu-id="0d71a-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="0d71a-136">**visFieldType**</span></span> <br/> |
   

