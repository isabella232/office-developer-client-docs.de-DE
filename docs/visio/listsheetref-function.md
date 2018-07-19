---
title: LISTSHEETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Gibt eine Blattreferenz auf das Listencontainer-Shape zurück, das das Shape enthält.
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797373"
---
# <a name="listsheetref-function"></a><span data-ttu-id="44e6a-103">LISTSHEETREF Function</span><span class="sxs-lookup"><span data-stu-id="44e6a-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="44e6a-104">Gibt eine Blattreferenz auf das Listencontainer-Shape zurück, das das Shape enthält.</span><span class="sxs-lookup"><span data-stu-id="44e6a-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="44e6a-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="44e6a-105">Version Information</span></span>

<span data-ttu-id="44e6a-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="44e6a-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="44e6a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="44e6a-107">Syntax</span></span>

<span data-ttu-id="44e6a-108">LISTMEMBERCOUNT()</span><span class="sxs-lookup"><span data-stu-id="44e6a-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="44e6a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44e6a-109">Return value</span></span>

<span data-ttu-id="44e6a-110">ShapeSheet-Referenz</span><span class="sxs-lookup"><span data-stu-id="44e6a-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44e6a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44e6a-111">Remarks</span></span>

<span data-ttu-id="44e6a-112">Wenn es sich bei dem Shape nicht um ein Listenelement handelt, gibt die LISTSHEETREF-Funktion #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="44e6a-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="44e6a-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="44e6a-113">Example</span></span>

<span data-ttu-id="44e6a-114">LISTSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="44e6a-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="44e6a-115">Gibt den Werte in der Zelle "Height" des Listencontainer-Shapes zurück, das das Shape enthält.</span><span class="sxs-lookup"><span data-stu-id="44e6a-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  

