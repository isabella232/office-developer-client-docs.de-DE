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
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797317"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="df26e-103">LangID Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="df26e-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="df26e-104">Gibt die Sprache an, in der Zellformeln erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="df26e-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="df26e-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df26e-105">Remarks</span></span>

<span data-ttu-id="df26e-106">Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie unter dem Thema [DocLangID](doclangid-cell-document-properties-section.md) Zelle (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="df26e-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="df26e-107">Wenn Sie einen Verweis auf die Zelle LangID nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="df26e-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df26e-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="df26e-108">Cell name:</span></span>  <br/> | <span data-ttu-id="df26e-109">LangID</span><span class="sxs-lookup"><span data-stu-id="df26e-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="df26e-110">Wenn Sie einen Verweis auf die Zelle LangID aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="df26e-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df26e-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="df26e-111">Section index:</span></span>  <br/> |<span data-ttu-id="df26e-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="df26e-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="df26e-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="df26e-113">Row index:</span></span>  <br/> |<span data-ttu-id="df26e-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="df26e-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="df26e-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="df26e-115">Cell index:</span></span>  <br/> |<span data-ttu-id="df26e-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="df26e-116">**visObjLangID**</span></span> <br/> |
   

