---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Ruft ein Array von Bytes ab, das die Bildressource für die Person enthält.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406710"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="e914d-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="e914d-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="e914d-104">Ruft ein Array von Bytes ab, das die Bildressource für die Person enthält.</span><span class="sxs-lookup"><span data-stu-id="e914d-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="e914d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="e914d-105">Parameters</span></span>

<span data-ttu-id="e914d-106">_picture_</span><span class="sxs-lookup"><span data-stu-id="e914d-106">_picture_</span></span>
  
> <span data-ttu-id="e914d-107">[out] Ein Zeiger auf eine Struktur, die ein Bytearray angibt, das die Bildressource für eine Person repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="e914d-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e914d-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e914d-108">Remarks</span></span>

<span data-ttu-id="e914d-109">Unterstützte Bildressourcen befinden sich im .bmp, JPEG oder .png Format.</span><span class="sxs-lookup"><span data-stu-id="e914d-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e914d-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e914d-110">See also</span></span>

- [<span data-ttu-id="e914d-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e914d-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

