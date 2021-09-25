---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Ruft ein Bytearray ab, das die Bildressource für die Person enthält.
ms.openlocfilehash: 090dae46f97c2b937155d61ec65b87f2c635da5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629158"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Ruft ein Bytearray ab, das die Bildressource für die Person enthält. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Parameter

_Bild_
  
> [out] Ein Zeiger auf eine Struktur, die ein Bytearray angibt, das die Bildressource für eine Person darstellt.
    
## <a name="remarks"></a>Bemerkungen

Unterstützte Bildressourcen haben das Format .bmp, JPEG oder .png.
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

