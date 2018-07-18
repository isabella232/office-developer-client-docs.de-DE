---
title: Zelle "Type" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: Gibt einen Datentyp für den Shape-Datenwert an.
ms.openlocfilehash: e5471dcc1ed487a5992779f1faa4763887bebb2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798327"
---
# <a name="type-cell-shape-data-section"></a><span data-ttu-id="6fdcf-103">Type Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="6fdcf-103">Type Cell (Shape Data Section)</span></span>

<span data-ttu-id="6fdcf-104">Gibt einen Datentyp für den Shape-Datenwert an.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-104">Specifies a data type for the shape data value.</span></span>
  
|<span data-ttu-id="6fdcf-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-105">**Value**</span></span>|<span data-ttu-id="6fdcf-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-106">**Description**</span></span>|<span data-ttu-id="6fdcf-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fdcf-108">0</span><span class="sxs-lookup"><span data-stu-id="6fdcf-108">0</span></span>  <br/> |<span data-ttu-id="6fdcf-p101">Zeichenfolge. Dies ist der Standard.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-p101">String. This is the default.</span></span>  <br/> |<span data-ttu-id="6fdcf-111">**visPropTypeString**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-111">**visPropTypeString**</span></span> <br/> |
|<span data-ttu-id="6fdcf-112">1</span><span class="sxs-lookup"><span data-stu-id="6fdcf-112">1</span></span>  <br/> |<span data-ttu-id="6fdcf-p102">Feste Liste. Zeigt die Listenelemente in einem Dropdown-Kombinationsfeld im Dialogfeld Shape-Daten definieren an. Geben Sie die Listenelemente in der Zelle Format an. Benutzer können nur ein Element aus der Liste auswählen.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-p102">Fixed list. Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box. Specify the list items in the Format cell. Users can select only one item from the list.  </span></span><br/> |<span data-ttu-id="6fdcf-117">**visPropTypeListFix**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-117">**visPropTypeListFix**</span></span> <br/> |
|<span data-ttu-id="6fdcf-118">2</span><span class="sxs-lookup"><span data-stu-id="6fdcf-118">2</span></span>  <br/> |<span data-ttu-id="6fdcf-p103">Number. Enthält Datum, Uhrzeit, Zeitdauer, Währungs- und Skalarwerte sowie Maß- und Winkelangaben. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-p103">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="6fdcf-122">**visPropTypeNumber**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-122">**visPropTypeNumber**</span></span> <br/> |
|<span data-ttu-id="6fdcf-123">3</span><span class="sxs-lookup"><span data-stu-id="6fdcf-123">3</span></span>  <br/> |<span data-ttu-id="6fdcf-p104">Boolescher Wert. Zeigt FALSE oder TRUE als Elemente an, die Benutzer aus einem Dropdown-Listenfeld im Dialogfeld Shape-Daten definieren auswählen können.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-p104">Boolean. Displays FALSE and TRUE as items users can select from a drop-down list box in the **Define Shape Data** dialog box.  </span></span><br/> |<span data-ttu-id="6fdcf-126">**visPropTypeBool**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-126">**visPropTypeBool**</span></span> <br/> |
|<span data-ttu-id="6fdcf-127">4</span><span class="sxs-lookup"><span data-stu-id="6fdcf-127">4</span></span>  <br/> |<span data-ttu-id="6fdcf-p105">Variable Liste. Zeigt die Listenelemente in einem Dropdown-Kombinationsfeld im Dialogfeld Shape-Daten definieren an. Geben Sie die Listenelemente in der Zelle Format an. Benutzer können entweder ein Listenelement auswählen oder ein neues Element eingeben, das der aktuellen Liste in der Zelle Format hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-p105">Variable list. Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box. Specify the list items in the Format cell. Users can select a list item or enter a new item that is added to the current list in the Format cell.  </span></span><br/> |<span data-ttu-id="6fdcf-132">**visPropTypeListVar**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-132">**visPropTypeListVar**</span></span> <br/> |
|<span data-ttu-id="6fdcf-133">5</span><span class="sxs-lookup"><span data-stu-id="6fdcf-133">5</span></span>  <br/> |<span data-ttu-id="6fdcf-p106">Datums- oder Uhrzeitwert. Zeigt Tage, Monate und Jahre oder Sekunden, Minuten und Stunden bzw. einen gemischten Datums- und Uhrzeitwert an. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-p106">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="6fdcf-137">**visPropTypeDate**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-137">**visPropTypeDate**</span></span> <br/> |
|<span data-ttu-id="6fdcf-138">6</span><span class="sxs-lookup"><span data-stu-id="6fdcf-138">6</span></span>  <br/> |<span data-ttu-id="6fdcf-p107">Zeitdauerwert. Zeigt die verstrichene Zeit an. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-p107">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="6fdcf-142">**visPropTypeDuration**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-142">**visPropTypeDuration**</span></span> <br/> |
|<span data-ttu-id="6fdcf-143">7</span><span class="sxs-lookup"><span data-stu-id="6fdcf-143">7</span></span>  <br/> |<span data-ttu-id="6fdcf-p108">Währungswert. Verwendet die aktuellen Landes-/Regionaleinstellungen des Systems. Geben Sie in der Zelle Format eine Formatierungsangabe an.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-p108">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="6fdcf-147">**visPropTypeCurrency**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-147">**visPropTypeCurrency**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fdcf-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fdcf-148">Remarks</span></span>

<span data-ttu-id="6fdcf-149">Wenn Sie einen Verweis auf die Zelle Type aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6fdcf-149">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6fdcf-150">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6fdcf-150">Cell name:</span></span>  <br/> |<span data-ttu-id="6fdcf-151">Eigenschaft. *Name* . Typ wobei Prop.  *Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="6fdcf-151">Prop. *Name*  .Type where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6fdcf-152">Wenn Sie einen Verweis auf die Zelle Type aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6fdcf-152">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6fdcf-153">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6fdcf-153">Section index:</span></span>  <br/> |<span data-ttu-id="6fdcf-154">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-154">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="6fdcf-155">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6fdcf-155">Row index:</span></span>  <br/> |<span data-ttu-id="6fdcf-156">**VisRowProp** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6fdcf-156">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6fdcf-157">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6fdcf-157">Cell index:</span></span>  <br/> |<span data-ttu-id="6fdcf-158">**visCustPropsType**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-158">**visCustPropsType**</span></span> <br/> |
   

