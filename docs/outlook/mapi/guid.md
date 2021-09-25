---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8be044edc628143bc7f7a4a33caa1046f0a3e5e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561740"
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

## <a name="members"></a>Members

 **Data1**
  
> Ein unsigned long integer data value.
    
 **Data2**
  
> Ein unsigned short integer data value.
    
 **Data3**
  
> Ein unsigned short integer data value.
    
 **Daten4**
  
> Ein Array von nicht signierten Zeichen.
    
## <a name="remarks"></a>HinwBemerkungeneise

 **GUID-Strukturen** werden in der MAPI wie folgt verwendet: 
  
- In den [MAPIUID-Strukturen,](mapiuid.md) die Dienstanbieter eindeutig identifizieren. 
    
- Für Schnittstellenbezeichner.
    
- In den Eigenschaftensatznamen benannter Eigenschaften. 
    
Nachrichtenspeicher- und Adressbuchanbieter generieren eine **GUID-Struktur,** die in ihrer **MAPIUID-Struktur** verwendet werden soll. Durch Übergeben der resultierenden **MAPIUID** an [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)informieren diese Dienstanbieter die MAPI über ihren eindeutigen Bezeichner.
  
Sie werden auch bei der Implementierung von Microsoft Remote Procedure Call (RPC) und der Object Description Language (ODL) verwendet. Weitere Informationen zu diesen Verwendungen finden Sie im  *Microsoft RPC Programmer's Guide and Reference*, OLE *Programmer's Reference*  und Inside  *OLE*, *Second Edition*  . 
  
Die **GUID-Struktur** ist in der  *Win32-Programmierreferenz*  definiert. Bestimmte Werte für **GUID-Strukturen,** die in der MAPI verwendet werden, werden in der MAPI-Headerdatei Mapiguid.h definiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[MAPI-Strukturen](mapi-structures.md)

