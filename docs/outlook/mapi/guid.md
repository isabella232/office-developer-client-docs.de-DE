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
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299517"
---
# <a name="guid"></a>GUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine GUID (Globally Unique Identifier). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiguid. h  <br/> |
   
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
  
> Ein Datenwert mit langer Ganzzahl ohne Vorzeichen.
    
 **Data2**
  
> Ein unsigned Short Integer-Datenwert.
    
 **Data3**
  
> Ein unsigned Short Integer-Datenwert.
    
 **Data4**
  
> Ein Array mit nicht signierten Zeichen.
    
## <a name="remarks"></a>Bemerkungen

 **GUID** -Strukturen werden in MAPI wie folgt verwendet: 
  
- In den [MAPIUID](mapiuid.md) -Strukturen, die Dienstanbieter eindeutig identifizieren. 
    
- Für Schnittstellenbezeichner.
    
- In den Eigenschaftensatz Namen benannter Eigenschaften. 
    
Nachrichtenspeicher-und Adressbuchanbieter generieren eine **GUID** -Struktur, die in Ihrer **MAPIUID** -Struktur verwendet werden soll. Durch das Übergeben des resultierenden **MAPIUID** an [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md)informieren diese Dienstanbieter MAPI über Ihren eindeutigen Bezeichner.
  
Außerdem werden Sie bei der Implementierung von Microsoft Remote Procedure Call (RPC) und der Object Description Language (ODL) verwendet. Weitere Informationen zu diesen Zwecken finden Sie im *Microsoft RPC Programmer es Guide and Reference*, *OLE Programmer es Reference* und *Inside OLE*, *Second Edition* . 
  
Die **GUID** -Struktur ist in der *Win32-Programmierreferenz* definiert. Bestimmte Werte für **GUID** -Strukturen, die in MAPI verwendet werden, sind in der MAPI-Headerdatei Mapiguid. h definiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[MAPI-Strukturen](mapi-structures.md)

