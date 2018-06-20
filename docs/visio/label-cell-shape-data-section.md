---
title: Zelle "Label" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Gibt die Beschriftung, die für Benutzer im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich des Unterstrich (_).
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797257"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="d601a-104">Label Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="d601a-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="d601a-105">Gibt die Beschriftung, die für Benutzer im Fenster **Shape-Daten** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d601a-105">Specifies the label that appears to users in the **Shape Data** window.</span></span> <span data-ttu-id="d601a-106">Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich des Unterstrich (_).</span><span class="sxs-lookup"><span data-stu-id="d601a-106">A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d601a-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d601a-107">Remarks</span></span>

<span data-ttu-id="d601a-108">Die Anwendung schließt die Beschriftungszeichenfolge automatisch in Anführungszeichen in der Zelle, aber diese Anführungszeichen werden im Fenster **Shape-Daten** nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d601a-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="d601a-109">Wird kein Beschriftungstext gefunden wird, zeigt Visio den Zeilennamen (Prop.Row) im Fenster **Shape-Daten** an.</span><span class="sxs-lookup"><span data-stu-id="d601a-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="d601a-110">Wenn Sie einen Verweis auf die Zelle Label nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d601a-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d601a-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d601a-111">Cell name:</span></span>  <br/> |<span data-ttu-id="d601a-112">Eigenschaft. *Name* . Beschriftung wobei Prop.  *Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="d601a-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d601a-113">Wenn Sie einen Verweis auf die Zelle Label aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d601a-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d601a-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d601a-114">Section index:</span></span>  <br/> |<span data-ttu-id="d601a-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="d601a-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="d601a-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d601a-116">Row index:</span></span>  <br/> |<span data-ttu-id="d601a-117">**VisRowProp** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d601a-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d601a-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d601a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d601a-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="d601a-119">**visCustPropsLabel**</span></span> <br/> |
   

