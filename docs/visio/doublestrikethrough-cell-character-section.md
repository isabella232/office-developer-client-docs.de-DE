---
title: Zelle "DoubleStrikethrough" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Legt fest, ob der Text doppelt durchgestrichen formatiert ist.
ms.openlocfilehash: dcd7c7769da8298c1f6ab474d2b63fc982f479b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796901"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="e69bf-103">DoubleStrikethrough Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="e69bf-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="e69bf-104">Legt fest, ob der Text doppelt durchgestrichen formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="e69bf-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e69bf-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e69bf-105">Remarks</span></span>

<span data-ttu-id="e69bf-106">Wenn Sie einen Verweis auf die Zelle DoubleStrikethrough aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e69bf-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e69bf-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e69bf-107">Cell name:</span></span>  <br/> | <span data-ttu-id="e69bf-108">Char.DoubleStrikethrough [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e69bf-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e69bf-109">Wenn Sie einen Verweis auf die Zelle DoubleStrikethrough aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e69bf-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e69bf-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e69bf-110">Section index:</span></span>  <br/> |<span data-ttu-id="e69bf-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="e69bf-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="e69bf-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e69bf-112">Row index:</span></span>  <br/> |<span data-ttu-id="e69bf-113">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e69bf-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e69bf-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e69bf-114">Cell index:</span></span>  <br/> |<span data-ttu-id="e69bf-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="e69bf-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

