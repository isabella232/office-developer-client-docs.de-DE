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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421585"
---
# <a name="guid"></a>GUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine GUID (Globally Unique Identifier). 
  
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
  
> Ein nicht signierter ganzzahliger Datenwert für lange Zahlen.
    
 **Data2**
  
> Ein nicht signierter ganzzahliger Datenwert ohne Vorzeichen.
    
 **Data3**
  
> Ein nicht signierter ganzzahliger Datenwert ohne Vorzeichen.
    
 **Data4**
  
> Ein Array von nicht signierten Zeichen.
    
## <a name="remarks"></a>Hinweise

 **GUID-Strukturen** werden in MAPI wie folgt verwendet: 
  
- In den [MAPIUID-Strukturen,](mapiuid.md) die Dienstanbieter eindeutig identifizieren. 
    
- Für Schnittstellenbezeichner.
    
- In der Eigenschaftensatznamen benannter Eigenschaften. 
    
Nachrichtenspeicher- und Adressbuchanbieter generieren eine **GUID-Struktur,** die in ihrer **MAPIUID-Struktur verwendet werden** soll. Durch Übergeben der resultierenden **MAPIUID** an [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)informieren diese Dienstanbieter MAPI über ihren eindeutigen Bezeichner.
  
Außerdem werden sie in der Implementierung von Microsoft Remote Procedure Call (RPC) und der Object Description Language (ODL) verwendet. Weitere Informationen zu diesen Verwendungen finden Sie im  *Microsoft RPC Programmer's Guide and Reference*, OLE *Programmer's Reference*  und Inside  *OLE*, *Second Edition*  . 
  
Die **GUID-Struktur** ist in der *Win32-Programmierreferenz definiert.* Spezifische Werte für **GUID-Strukturen,** die in MAPI verwendet werden, werden in der MAPI-Headerdatei Mapiguid.h definiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[MAPI-Strukturen](mapi-structures.md)

