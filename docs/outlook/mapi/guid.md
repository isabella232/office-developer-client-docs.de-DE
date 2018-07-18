---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 08ecb718572944db07c2888e0aae1464bd5c0f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791801"
---
# <a name="guid"></a>GUID

  
  
**Betrifft**: Outlook 
  
Beschreibt einen global eindeutigen Bezeichner (GUID). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiguid.h  <br/> |
   
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

 **Data1**
  
> Eine lange Ganzzahl ohne Vorzeichen Datenwert.
    
 **Data2**
  
> Eine ganze Zahl ohne Vorzeichen kurzen Datenwert.
    
 **Data3**
  
> Eine ganze Zahl ohne Vorzeichen kurzen Datenwert.
    
 **Data4**
  
> Ein Array von nicht signierte Zeichen.
    
## <a name="remarks"></a>Bemerkungen

 **GUID** -Strukturen werden in MAPI wie folgt verwendet: 
  
- In den [MAPIUID](mapiuid.md) -Strukturen, mit die Dienstanbieter eindeutig identifiziert. 
    
- Schnittstelle-Bezeichner.
    
- Legen in die Eigenschaft Namen der benannten Eigenschaften. 
    
Nachrichtenspeicher und Adresse adressbuchanbietern implementierte generieren eine **GUID** -Struktur, die in ihrer **MAPIUID** Struktur verwendet. Informieren Sie, indem Sie die resultierende **MAPIUID** an [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)übergeben, dieser Dienstanbieter MAPI der jeweiligen eindeutigen Bezeichner.
  
Darüber hinaus werden sie in der Implementierung von Microsoft Remote Procedure Call (RPC) sowie dem Objekt Description Language () verwendet. Weitere Informationen zu diesen verwendet finden Sie unter der *Microsoft RPC Programmer's Guide und Verweis* *OLE Programmer's Reference* und *In OLE*, *Second Edition* . 
  
Die **GUID** -Struktur ist in der *Win32 Programmer's Reference* definiert. Konkrete Werte für die **GUID** -Strukturen, die in MAPI verwendet werden, werden in der MAPI-Headerdatei Mapiguid.h definiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[MAPI-Strukturen](mapi-structures.md)

