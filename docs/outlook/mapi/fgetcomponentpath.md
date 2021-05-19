---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335210"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Pfad zum privaten Mapi32.dll.
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a>Parameter

 _szComponent_
  
> [in] Der MSIComponentID-Reg-Schlüssel, der unter [Mapi32.dll Stub registry Einstellungen](https://msdn.microsoft.com/library/dd162409.aspx).
    
 _szQualifier_
  
> [in] Der unter [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md)beschriebene Unterschlüssel MSIApplicationLCID oder MSIOfficeLCID. Anrufer können **null übergeben,** wenn kein Qualifizierer vorlägig ist. 
    
 _szDllPath_
  
> [in] Der Pfad zum privaten Mapi32.dll, der über vollständige MAPI-Funktionen verfügt (der gleiche Export wie der Mapi32.dll).
    
 _cchBufferSize_
  
> [in] Die Größe von  _szDllPath_ in Zeichen.
    
 _fInstall_
  
> [in] Weist MAPI an, die private Mapi32.dll zu installieren, wenn sie nicht vorhanden ist.
    
## <a name="return-value"></a>Rückgabewert

 **true**
  
> Der Pfad wurde gefunden.
    
 **false**
  
> Der Pfad wurde nicht gefunden.
    
## <a name="remarks"></a>Hinweise

Verwenden Sie **die FGetComponentPath-Funktion,** wenn Sie den Pfad zum privaten Mapi32.dll. 
  
## <a name="see-also"></a>Siehe auch



[Auswählen einer bestimmten Version der zu ladende MAPI](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll stub Registry Einstellungen](https://msdn.microsoft.com/library/dd162409.aspx)

