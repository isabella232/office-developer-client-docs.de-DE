---
title: Zelle "LangID" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Gibt die Sprache an, in der der Text eingegeben wurde.
ms.openlocfilehash: e503abb2365635fa25a4dbec54b7fe3da4043fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797274"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="2d244-103">Zelle "LangID" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="2d244-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="2d244-104">Gibt die Sprache an, in der der Text eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2d244-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d244-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d244-105">Remarks</span></span>

<span data-ttu-id="2d244-106">Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie unter dem Thema [DocLangID](doclangid-cell-document-properties-section.md) Zelle (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="2d244-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="2d244-107">Wenn Sie einen Verweis auf die Zelle LangID nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2d244-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d244-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2d244-108">Cell name:</span></span>  <br/> | <span data-ttu-id="2d244-109">Char.LangID [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2d244-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2d244-110">Wenn Sie einen Verweis auf die Zelle LangID aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2d244-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d244-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2d244-111">Section index:</span></span>  <br/> |<span data-ttu-id="2d244-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="2d244-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="2d244-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2d244-113">Row index:</span></span>  <br/> |<span data-ttu-id="2d244-114">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2d244-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2d244-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2d244-115">Cell index:</span></span>  <br/> |<span data-ttu-id="2d244-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="2d244-116">**visCharacterLangID**</span></span> <br/> |
   

