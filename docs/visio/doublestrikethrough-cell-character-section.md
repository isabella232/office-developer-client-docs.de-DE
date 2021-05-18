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
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360592"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="937f7-103">Zelle "DoubleStrikethrough" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="937f7-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="937f7-104">Legt fest, ob der Text doppelt durchgestrichen formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="937f7-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="937f7-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="937f7-105">Remarks</span></span>

<span data-ttu-id="937f7-106">Um einen Verweis auf die Zelle DoubleStrikethrough anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="937f7-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="937f7-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="937f7-107">Cell name:</span></span>  <br/> | <span data-ttu-id="937f7-108">Char.DoubleStrikethrough[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="937f7-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="937f7-109">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DoubleStrikethrough-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="937f7-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="937f7-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="937f7-110">Section index:</span></span>  <br/> |<span data-ttu-id="937f7-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="937f7-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="937f7-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="937f7-112">Row index:</span></span>  <br/> |<span data-ttu-id="937f7-113">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="937f7-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="937f7-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="937f7-114">Cell index:</span></span>  <br/> |<span data-ttu-id="937f7-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="937f7-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

