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
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431519"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="6d8de-103">Zelle "Format" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="6d8de-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="6d8de-104">Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.</span><span class="sxs-lookup"><span data-stu-id="6d8de-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d8de-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6d8de-105">Remarks</span></span>

<span data-ttu-id="6d8de-106">Wenn der Wert der Zelle Type 0, 2, 5, 6 oder 7 (Zeichenfolge, Zahl, Datum oder Uhrzeit, Dauer oder Währung) ist, geben Sie ein Formatbild an, das für den Datentyp geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="6d8de-106">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type.</span></span> <span data-ttu-id="6d8de-107">Beispielsweise formatiert das Formatbild "# #/4 UU" die Zahl 12,43 zoll.</span><span class="sxs-lookup"><span data-stu-id="6d8de-107">For example, the format picture "# #/4 UU" formats the number 12.43 in.</span></span> <span data-ttu-id="6d8de-108">als 12 2/4 ZOLL.</span><span class="sxs-lookup"><span data-stu-id="6d8de-108">as 12 2/4 INCHES.</span></span> <span data-ttu-id="6d8de-109">Weitere Informationen zum Festlegen von Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="6d8de-109">For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="6d8de-p102">Eine Zahl (Typ = 2) kann einen Bemaßungs-, Skalar-, Winkel-, Datums-, Zeit- oder Währungswert darstellen. Wenn Sie sicherstellen möchten, dass eine eingegebene Zahl immer als Datum, Uhrzeit oder Währung gewertet wird, verwenden Sie anstelle einer Formatierungsangabe die Funktionen DATETIME oder CY in der Zelle Format.</span><span class="sxs-lookup"><span data-stu-id="6d8de-p102">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="6d8de-112">Um einen Verweis auf die Zelle Format anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="6d8de-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d8de-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6d8de-113">Cell name:</span></span>  <br/> | <span data-ttu-id="6d8de-114">Fields.Format[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6d8de-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6d8de-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Format nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="6d8de-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d8de-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6d8de-116">Section index:</span></span>  <br/> |<span data-ttu-id="6d8de-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="6d8de-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="6d8de-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6d8de-118">Row index:</span></span>  <br/> |<span data-ttu-id="6d8de-119">**visRowField**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6d8de-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6d8de-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6d8de-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6d8de-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="6d8de-121">**visFieldFormat**</span></span> <br/> |
   

