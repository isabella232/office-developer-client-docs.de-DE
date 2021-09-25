---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c73dac549ec54d7e2dfd67a1f54031001a77684e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630817"
---
# <a name="iid"></a>IID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine [GUID-Struktur,](guid.md) mit der ein Bezeichner für eine MAPI-Schnittstelle beschrieben wird. 
  
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

Siehe **GUID-Struktur.** 
  
## <a name="remarks"></a>Bemerkungen

Eine **IID-Struktur** wird verwendet, um eine MAPI-Schnittstelle eindeutig zu identifizieren und eine bestimmte Schnittstelle einem Objekt zuzuordnen. Wenn ein Client beispielsweise [IMAPISession::OpenEntry](imapisession-openentry.md) aufruft, um einen Ordner zu öffnen, legt der Client den  _LpInterface-Parameter_ so fest, dass er auf eine **IID** zeigt, die die [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) darstellt. MAPI definiert die **IMAPIFolderIID** als IID_IMAPIFolder. **IID-Strukturen** werden auch verwendet, um OLE-Schnittstellen eindeutig zu identifizieren. 
  
Alle spezifischen **IID-Strukturen** für die MAPI-Schnittstellen sind in der Headerdatei Mapiguid.h definiert. 
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)


[MAPI-Strukturen](mapi-structures.md)

