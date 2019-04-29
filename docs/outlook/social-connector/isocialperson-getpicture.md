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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406710"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Ruft ein Bytearray ab, das die Bildressource für die Person enthält. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Parameter

_Bild_
  
> Out Ein Zeiger auf eine Struktur, die ein Bytearray angibt, das die Bildressource für eine Person darstellt.
    
## <a name="remarks"></a>Bemerkungen

Unterstützte Bildressourcen befinden sich im BMP-, JPEG-oder PNG-Format.
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

