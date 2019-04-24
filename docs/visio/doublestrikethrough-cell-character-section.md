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
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="a19c3-103">Zelle "DoubleStrikethrough" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="a19c3-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="a19c3-104">Legt fest, ob der Text doppelt durchgestrichen formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="a19c3-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a19c3-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a19c3-105">Remarks</span></span>

<span data-ttu-id="a19c3-106">Wenn Sie einen Verweis auf die Zelle DoubleStrikethrough aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a19c3-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a19c3-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a19c3-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a19c3-108">Char. DoubleStrikethrough [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a19c3-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a19c3-109">Wenn Sie einen Verweis auf die Zelle DoubleStrikethrough aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a19c3-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a19c3-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a19c3-110">Section index:</span></span>  <br/> |<span data-ttu-id="a19c3-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="a19c3-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="a19c3-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a19c3-112">Row index:</span></span>  <br/> |<span data-ttu-id="a19c3-113">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a19c3-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a19c3-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a19c3-114">Cell index:</span></span>  <br/> |<span data-ttu-id="a19c3-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="a19c3-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

