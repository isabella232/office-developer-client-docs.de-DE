---
title: Zelle "PaperKind" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Gibt den Papiertyp für den Druck der Seite an.
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797597"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="dab99-103">Zelle "PaperKind" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="dab99-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="dab99-104">Gibt den Papiertyp für den Druck der Seite an.</span><span class="sxs-lookup"><span data-stu-id="dab99-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dab99-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dab99-105">Remarks</span></span>

<span data-ttu-id="dab99-106">Diese Einstellung entspricht der Einstellung **Papiergröße** im Dialogfeld **Drucker einrichten** (klicken Sie auf der Registerkarte **Entwurf** , klicken Sie auf den Pfeil neben **Seite einrichten** , und klicken Sie dann auf der Registerkarte **Druckeinrichtung** auf die Schaltfläche " **Setup** ").</span><span class="sxs-lookup"><span data-stu-id="dab99-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="dab99-107">Die numerischen Werte in dieser Zelle auf Konstanten (mit dem Präfix DMPAPER) in der Microsoft Windows-Datei wingdi.h für die Papierauswahl definiert sind.</span><span class="sxs-lookup"><span data-stu-id="dab99-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="dab99-108">Wenn Sie einen Verweis auf die Zelle PaperKind nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dab99-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dab99-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dab99-109">Cell name:</span></span>  <br/> |<span data-ttu-id="dab99-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="dab99-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="dab99-111">Wenn Sie einen Verweis auf die Zelle PaperKind aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dab99-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dab99-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dab99-112">Section index:</span></span>  <br/> |<span data-ttu-id="dab99-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dab99-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dab99-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dab99-114">Row index:</span></span>  <br/> |<span data-ttu-id="dab99-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="dab99-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="dab99-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dab99-116">Cell index:</span></span>  <br/> |<span data-ttu-id="dab99-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="dab99-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

