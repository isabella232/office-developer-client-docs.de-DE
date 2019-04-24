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
  
Gibt den Pfad zur privaten Mapi32. dll zurück.
  
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
  
> in Der MSIComponentID reg-Schlüssel, der in den [Mapi32. dll-Registrierungseinstellungen](https://msdn.microsoft.com/library/dd162409.aspx)beschrieben wird.
    
 _szQualifier_
  
> in Der Unterschlüssel MSIApplicationLCID oder MSIOfficeLCID, der in [Wählen Sie eine bestimmte Version von MAPI zum Laden](how-to-choose-a-specific-version-of-mapi-to-load.md)beschrieben. Aufrufer können **null** , wenn kein Qualifizierer vorhanden ist. 
    
 _szDllPath_
  
> in Der Pfad zur privaten Mapi32. dll, die vollständige MAPI-Funktionalität aufweist (derselbe Export wie der Mapi32. dll).
    
 _cchBufferSize_
  
> in Die Größe von _szDllPath_in Zeichen.
    
 _fInstall_
  
> in Weist MAPI an, die private Mapi32. dll-Komponente zu installieren, wenn Sie nicht vorhanden ist.
    
## <a name="return-value"></a>Rückgabewert

 **true**
  
> Der Pfad wurde gefunden.
    
 **false**
  
> Der Pfad wurde nicht gefunden.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **FGetComponentPath** -Funktion, wenn Sie den Pfad zur privaten Mapi32. dll abrufen müssen. 
  
## <a name="see-also"></a>Siehe auch



[Auswählen einer bestimmten zu ladenden MAPI-Version](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32. dll-Stub-Registrierungseinstellungen](https://msdn.microsoft.com/library/dd162409.aspx)

