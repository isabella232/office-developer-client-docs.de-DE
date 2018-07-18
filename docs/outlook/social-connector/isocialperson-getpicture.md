---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Ruft ein Array von Bytes, die die Bildressource der Person enthält.
ms.openlocfilehash: dcb0da5bc36c2166d569c770d1f182cd21339435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795964"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="490dd-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="490dd-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="490dd-104">Ruft ein Array von Bytes, die die Bildressource der Person enthält.</span><span class="sxs-lookup"><span data-stu-id="490dd-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="490dd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="490dd-105">Parameters</span></span>

<span data-ttu-id="490dd-106">_Bild_</span><span class="sxs-lookup"><span data-stu-id="490dd-106">_picture_</span></span>
  
> <span data-ttu-id="490dd-107">[out] Ein Zeiger auf eine Struktur, die ein Bytearray gibt an, die die Bildressource einer Person darstellen.</span><span class="sxs-lookup"><span data-stu-id="490dd-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="490dd-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="490dd-108">Remarks</span></span>

<span data-ttu-id="490dd-109">Grafik, die Ressourcen in BMP, JPEG oder PNG-Format werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="490dd-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="490dd-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="490dd-110">See also</span></span>

- [<span data-ttu-id="490dd-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="490dd-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

