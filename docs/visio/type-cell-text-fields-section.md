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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407984"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="0eeb5-103">Zelle "Type" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="0eeb5-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="0eeb5-104">Gibt einen Datentyp für den Textfeldwert an.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="0eeb5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0eeb5-105">**Value**</span></span>|<span data-ttu-id="0eeb5-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0eeb5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0eeb5-107">0</span><span class="sxs-lookup"><span data-stu-id="0eeb5-107">0</span></span>  <br/> |<span data-ttu-id="0eeb5-108">Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-108">String.</span></span>  <br/> |
|<span data-ttu-id="0eeb5-109">2</span><span class="sxs-lookup"><span data-stu-id="0eeb5-109">2</span></span>  <br/> |<span data-ttu-id="0eeb5-p101">Number. Enthält Datum, Uhrzeit, Zeitdauer, Währungs- und Skalarwerte sowie Maß- und Winkelangaben. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0eeb5-113">5 </span><span class="sxs-lookup"><span data-stu-id="0eeb5-113">5</span></span>  <br/> |<span data-ttu-id="0eeb5-p102">Datums- oder Uhrzeitwert. Zeigt Tage, Monate und Jahre oder Sekunden, Minuten und Stunden bzw. einen gemischten Datums- und Uhrzeitwert an. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0eeb5-117">6 </span><span class="sxs-lookup"><span data-stu-id="0eeb5-117">6</span></span>  <br/> |<span data-ttu-id="0eeb5-p103">Zeitdauerwert. Zeigt die verstrichene Zeit an. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0eeb5-121">7 </span><span class="sxs-lookup"><span data-stu-id="0eeb5-121">7</span></span>  <br/> |<span data-ttu-id="0eeb5-p104">Währungswert. Verwendet die aktuelle Landes-/Regionaleinstellungen des Systems. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0eeb5-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0eeb5-125">Remarks</span></span>

<span data-ttu-id="0eeb5-126">Sie können den Wert dieser Zelle  auch im Dialogfeld Feld festlegen  (klicken Sie auf der Registerkarte Einfügen in der **Gruppe Text** auf **Feld** ).</span><span class="sxs-lookup"><span data-stu-id="0eeb5-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="0eeb5-127">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Type anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="0eeb5-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0eeb5-128">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0eeb5-128">Cell name:</span></span>  <br/> |<span data-ttu-id="0eeb5-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0eeb5-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0eeb5-130">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Type nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="0eeb5-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0eeb5-131">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0eeb5-131">Section index:</span></span>  <br/> |<span data-ttu-id="0eeb5-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="0eeb5-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="0eeb5-133">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0eeb5-133">Row index:</span></span>  <br/> |<span data-ttu-id="0eeb5-134">**visRowField**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0eeb5-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0eeb5-135">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0eeb5-135">Cell index:</span></span>  <br/> |<span data-ttu-id="0eeb5-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="0eeb5-136">**visFieldType**</span></span> <br/> |
   

