---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411596"
---
# <a name="iid"></a>IID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine [GUID](guid.md) -Struktur, die zur Beschreibung eines Bezeichners für eine MAPI-Schnittstelle verwendet wird. 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

Siehe die **GUID** -Struktur. 
  
## <a name="remarks"></a>Bemerkungen

Eine **IID** -Struktur wird verwendet, um eine MAPI-Schnittstelle eindeutig zu identifizieren und eine bestimmte Schnittstelle einem Objekt zuzuordnen. Wenn ein Client beispielsweise [IMAPISession:: OpenEntry](imapisession-openentry.md) zum Öffnen eines Ordners aufruft, wird der _lpInterface_ -Parameter so festgelegt, dass er auf eine **IID** zeigt, die die [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle darstellt. MAPI definiert die **IMAPIFolderIID** als IID_IMAPIFolder. **IID** -Strukturen werden auch verwendet, um OLE-Schnittstellen eindeutig zu identifizieren. 
  
Alle spezifischen **IID** -Strukturen für die MAPI-Schnittstellen sind in der Headerdatei Mapiguid. h definiert. 
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)


[MAPI-Strukturen](mapi-structures.md)

