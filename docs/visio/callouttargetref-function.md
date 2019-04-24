---
title: CALLOUTTARGETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337247"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="9f7c4-103">CALLOUTTARGETREF Function</span><span class="sxs-lookup"><span data-stu-id="9f7c4-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="9f7c4-104">Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="9f7c4-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="9f7c4-105">Version Information</span></span>

<span data-ttu-id="9f7c4-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="9f7c4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9f7c4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f7c4-107">Syntax</span></span>

<span data-ttu-id="9f7c4-108">CALLOUTTARGETREF ()!</span><span class="sxs-lookup"><span data-stu-id="9f7c4-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="9f7c4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f7c4-109">Return value</span></span>

<span data-ttu-id="9f7c4-110">ShapeSheet-Referenz</span><span class="sxs-lookup"><span data-stu-id="9f7c4-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f7c4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f7c4-111">Remarks</span></span>

<span data-ttu-id="9f7c4-112">Wenn es sich bei dem Shape nicht um ein Beschriftungs-Shape handelt oder wenn es nicht mit einem Ziel-Shape verknüpft ist, gibt CALLOUTTARGETREF #REF zurück.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="9f7c4-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9f7c4-113">Example</span></span>

<span data-ttu-id="9f7c4-114">CALLOUTTARGETREF ()! Höhe</span><span class="sxs-lookup"><span data-stu-id="9f7c4-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="9f7c4-115">Gibt den Wert in der Zelle Height des Shapes zurück, das mit der Beschriftung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

