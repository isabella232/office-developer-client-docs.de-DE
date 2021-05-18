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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423013"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="7298e-103">CALLOUTTARGETREF Function</span><span class="sxs-lookup"><span data-stu-id="7298e-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="7298e-104">Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.</span><span class="sxs-lookup"><span data-stu-id="7298e-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="7298e-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="7298e-105">Version Information</span></span>

<span data-ttu-id="7298e-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="7298e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7298e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7298e-107">Syntax</span></span>

<span data-ttu-id="7298e-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="7298e-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="7298e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7298e-109">Return value</span></span>

<span data-ttu-id="7298e-110">ShapeSheet-Referenz</span><span class="sxs-lookup"><span data-stu-id="7298e-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7298e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7298e-111">Remarks</span></span>

<span data-ttu-id="7298e-112">Wenn es sich bei dem Shape nicht um ein Callout-Shape handelt oder wenn es keinem Ziel-Shape zugeordnet ist, gibt CALLOUTTARGETREF #REF.</span><span class="sxs-lookup"><span data-stu-id="7298e-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="7298e-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7298e-113">Example</span></span>

<span data-ttu-id="7298e-114">CALLOUTTARGETREF()! Height</span><span class="sxs-lookup"><span data-stu-id="7298e-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="7298e-115">Gibt den Wert in der Zelle Height des Shapes zurück, das mit der Beschriftung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="7298e-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

