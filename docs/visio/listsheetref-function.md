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
# <a name="listsheetref-function"></a><span data-ttu-id="7d0d2-103">LISTSHEETREF Function</span><span class="sxs-lookup"><span data-stu-id="7d0d2-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="7d0d2-104">Gibt eine Blattreferenz auf das Listencontainer-Shape zurück, das das Shape enthält.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="7d0d2-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="7d0d2-105">Version Information</span></span>

<span data-ttu-id="7d0d2-106">Hinzugefügte Version: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="7d0d2-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7d0d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d0d2-107">Syntax</span></span>

<span data-ttu-id="7d0d2-108">LISTMEMBERCOUNT()</span><span class="sxs-lookup"><span data-stu-id="7d0d2-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="7d0d2-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7d0d2-109">Return value</span></span>

<span data-ttu-id="7d0d2-110">ShapeSheet-Referenz</span><span class="sxs-lookup"><span data-stu-id="7d0d2-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d0d2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d0d2-111">Remarks</span></span>

<span data-ttu-id="7d0d2-112">Wenn es sich bei dem Shape nicht um ein Listenelement handelt, gibt die LISTSHEETREF-Funktion #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="7d0d2-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d0d2-113">Example</span></span>

<span data-ttu-id="7d0d2-114">LISTSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="7d0d2-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="7d0d2-115">Gibt den Werte in der Zelle "Height" des Listencontainer-Shapes zurück, das das Shape enthält.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  

