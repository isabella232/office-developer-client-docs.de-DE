---
title: Zelle "Format" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.
ms.openlocfilehash: 767b658a9431dfab23d2df9bcfa6c83b52f48d75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797064"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="df4de-103">Format Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="df4de-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="df4de-104">Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.</span><span class="sxs-lookup"><span data-stu-id="df4de-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df4de-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df4de-105">Remarks</span></span>

<span data-ttu-id="df4de-p101">Wenn die Zelle Type den Wert 0, 2, 5, 6 oder 7 besitzt (Zeichenfolge, Zahl, Datum bzw. Uhrzeit, Dauer oder Währung), geben Sie eine dem Datentyp entsprechende Formatierungsangabe an. Die Formatierungsangabe "# #/4 UU" formatiert beispielsweise die Zahl 12,43 Zoll als 12 2/4 ZOLL. Weitere Informationen zum Festlegen einer Formatierungsangabe finden Sie unter Informationen zu Formatierungsangaben.</span><span class="sxs-lookup"><span data-stu-id="df4de-p101">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type. For example, the format picture "# #/4 UU" formats the number 12.43 in. as 12 2/4 INCHES. For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="df4de-p102">Eine Zahl (Typ = 2) kann einen Bemaßungs-, Skalar-, Winkel-, Datums-, Zeit- oder Währungswert darstellen. Wenn Sie sicherstellen möchten, dass eine eingegebene Zahl immer als Datum, Uhrzeit oder Währung gewertet wird, verwenden Sie anstelle einer Formatierungsangabe die Funktionen DATETIME oder CY in der Zelle Format.</span><span class="sxs-lookup"><span data-stu-id="df4de-p102">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="df4de-112">Wenn Sie einen Verweis auf die Zelle Format aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="df4de-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df4de-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="df4de-113">Cell name:</span></span>  <br/> | <span data-ttu-id="df4de-114">Fields.Format [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="df4de-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="df4de-115">Wenn Sie einen Verweis auf die Zelle Format aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="df4de-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df4de-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="df4de-116">Section index:</span></span>  <br/> |<span data-ttu-id="df4de-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="df4de-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="df4de-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="df4de-118">Row index:</span></span>  <br/> |<span data-ttu-id="df4de-119">**VisRowField** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="df4de-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="df4de-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="df4de-120">Cell index:</span></span>  <br/> |<span data-ttu-id="df4de-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="df4de-121">**visFieldFormat**</span></span> <br/> |
   

