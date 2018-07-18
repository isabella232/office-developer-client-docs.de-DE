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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792057"
---
# <a name="iid"></a>IID

  
  
**Betrifft**: Outlook 
  
Beschreibt eine [GUID](guid.md) -Struktur verwendet, um einen Bezeichner für die MAPI-Schnittstelle beschrieben. 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Elemente

Finden Sie unter der **GUID** -Struktur. 
  
## <a name="remarks"></a>Bemerkungen

Eine **IID** -Struktur dient zur eindeutigen Identifizierung eine MAPI-Schnittstelle und ein Objekt eine bestimmte Schnittstelle zugeordnet. Beispielsweise legt fest, wenn eine Client-Anrufe [IMAPISession::OpenEntry](imapisession-openentry.md) an einen Ordner zu öffnen, der Client den _LpInterface_ -Parameter auf **IID** zeigen, das [IMAPIFolder](imapifolderimapicontainer.md) Schnittstelle darstellt. MAPI definiert die **IMAPIFolderIID** um IID_IMAPIFolder werden. **IID** Strukturen werden auch verwendet, um OLE-Schnittstellen eindeutig zu identifizieren. 
  
Alle von der bestimmten **IID** Strukturen für die MAPI-Schnittstellen werden in der Headerdatei Mapiguid.h definiert. 
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)


[MAPI-Strukturen](mapi-structures.md)

