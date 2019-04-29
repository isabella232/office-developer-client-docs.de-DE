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
description: Legt die Beschriftung fest, die Benutzern im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420178"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="87600-104">Zelle "Label" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="87600-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="87600-105">Legt die Beschriftung fest, die Benutzern im Fenster **Shape-Daten** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="87600-105">Specifies the label that appears to users in the **Shape Data** window.</span></span> <span data-ttu-id="87600-106">Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).</span><span class="sxs-lookup"><span data-stu-id="87600-106">A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="87600-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87600-107">Remarks</span></span>

<span data-ttu-id="87600-108">Die Anwendung schließt die Beschriftungszeichenfolge in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden im Fenster **Shape-Daten** nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="87600-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="87600-109">Wenn kein Bezeichnungstext gefunden wird, zeigt Visio im Fenster **Shape-Daten** den Zeilennamen (Prop. Row) an.</span><span class="sxs-lookup"><span data-stu-id="87600-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="87600-110">Wenn Sie einen Verweis auf die Zelle Label aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="87600-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87600-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="87600-111">Cell name:</span></span>  <br/> |<span data-ttu-id="87600-112">Prop. *Name* . Bezeichnung, wobei Prop.  *Name* ist der Name der Zeile</span><span class="sxs-lookup"><span data-stu-id="87600-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="87600-113">Wenn Sie einen Verweis auf die Zelle Label aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="87600-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87600-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="87600-114">Section index:</span></span>  <br/> |<span data-ttu-id="87600-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="87600-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="87600-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="87600-116">Row index:</span></span>  <br/> |<span data-ttu-id="87600-117">**visRowProp** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="87600-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="87600-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="87600-118">Cell index:</span></span>  <br/> |<span data-ttu-id="87600-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="87600-119">**visCustPropsLabel**</span></span> <br/> |
   

