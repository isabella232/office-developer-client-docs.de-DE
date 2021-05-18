---
title: Zelle "LangID" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Gibt die Sprache an, in der Zellformeln erstellt wurden.
ms.openlocfilehash: e1e5b92f01e97bc63003a4b195c159a50f61e77b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406675"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="c0a7a-103">Zelle "LangID" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="c0a7a-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c0a7a-104">Gibt die Sprache an, in der Zellformeln erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c0a7a-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c0a7a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0a7a-105">Remarks</span></span>

<span data-ttu-id="c0a7a-106">Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie im Thema [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="c0a7a-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="c0a7a-107">Um einen Verweis auf die LangID-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="c0a7a-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0a7a-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c0a7a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c0a7a-109">LangID</span><span class="sxs-lookup"><span data-stu-id="c0a7a-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="c0a7a-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LangID-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c0a7a-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0a7a-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c0a7a-111">Section index:</span></span>  <br/> |<span data-ttu-id="c0a7a-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0a7a-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c0a7a-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c0a7a-113">Row index:</span></span>  <br/> |<span data-ttu-id="c0a7a-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c0a7a-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c0a7a-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c0a7a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c0a7a-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="c0a7a-116">**visObjLangID**</span></span> <br/> |
   

