---
title: CALLOUTTARGETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796550"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="0ea0a-103">CALLOUTTARGETREF Function</span><span class="sxs-lookup"><span data-stu-id="0ea0a-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="0ea0a-104">Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.</span><span class="sxs-lookup"><span data-stu-id="0ea0a-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="0ea0a-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="0ea0a-105">Version Information</span></span>

<span data-ttu-id="0ea0a-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="0ea0a-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0ea0a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ea0a-107">Syntax</span></span>

<span data-ttu-id="0ea0a-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="0ea0a-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="0ea0a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ea0a-109">Return value</span></span>

<span data-ttu-id="0ea0a-110">ShapeSheet-Referenz</span><span class="sxs-lookup"><span data-stu-id="0ea0a-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ea0a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ea0a-111">Remarks</span></span>

<span data-ttu-id="0ea0a-112">Wenn die Form nicht um eine Beschriftung-Shape ist oder wenn es nicht mit einem übergeordneten Shape verknüpft ist, gibt CALLOUTTARGETREF #REF zurück.</span><span class="sxs-lookup"><span data-stu-id="0ea0a-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="0ea0a-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0ea0a-113">Example</span></span>

<span data-ttu-id="0ea0a-114">CALLOUTTARGETREF()!Height</span><span class="sxs-lookup"><span data-stu-id="0ea0a-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="0ea0a-115">Gibt den Wert in der Zelle Height des Shapes zurück, das mit der Beschriftung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="0ea0a-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

