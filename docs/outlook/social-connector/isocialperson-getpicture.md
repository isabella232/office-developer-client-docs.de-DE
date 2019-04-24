---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Ruft ein Bytearray ab, das die Bildressource für die Person enthält.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331654"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="ab25c-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="ab25c-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="ab25c-104">Ruft ein Bytearray ab, das die Bildressource für die Person enthält.</span><span class="sxs-lookup"><span data-stu-id="ab25c-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="ab25c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab25c-105">Parameters</span></span>

<span data-ttu-id="ab25c-106">_Bild_</span><span class="sxs-lookup"><span data-stu-id="ab25c-106">_picture_</span></span>
  
> <span data-ttu-id="ab25c-107">Out Ein Zeiger auf eine Struktur, die ein Bytearray angibt, das die Bildressource für eine Person darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab25c-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab25c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab25c-108">Remarks</span></span>

<span data-ttu-id="ab25c-109">Unterstützte Bildressourcen befinden sich im BMP-, JPEG-oder PNG-Format.</span><span class="sxs-lookup"><span data-stu-id="ab25c-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab25c-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab25c-110">See also</span></span>

- [<span data-ttu-id="ab25c-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ab25c-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

