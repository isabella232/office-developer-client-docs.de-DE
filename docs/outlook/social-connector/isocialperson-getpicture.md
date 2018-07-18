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
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Ruft ein Array von Bytes, die die Bildressource der Person enthält. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Parameter

_Bild_
  
> [out] Ein Zeiger auf eine Struktur, die ein Bytearray gibt an, die die Bildressource einer Person darstellen.
    
## <a name="remarks"></a>Bemerkungen

Grafik, die Ressourcen in BMP, JPEG oder PNG-Format werden unterstützt.
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

