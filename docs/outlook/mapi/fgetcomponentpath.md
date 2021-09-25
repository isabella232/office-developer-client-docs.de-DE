---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0ad1e8ef09b3f41c46c0c321e0e3699e9e6020bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621101"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Pfad zum privaten Mapi32.dll zurück.
  
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
  
> [in] Der in [Mapi32.dll Stub Registry Einstellungen](https://msdn.microsoft.com/library/dd162409.aspx)beschriebene MSIComponentID-Registrierungsschlüssel.
    
 _szQualifier_
  
> [in] Der Unterschlüssel MSIApplicationLCID oder MSIOfficeLCID, der unter [Auswählen einer bestimmten Version von MAPI zum Laden](how-to-choose-a-specific-version-of-mapi-to-load.md)beschrieben ist. Aufrufer können **NULL** übergeben, wenn kein Qualifizierer vorhanden ist. 
    
 _szDllPath_
  
> [in] Der Pfad zum privaten Mapi32.dll, der über vollständige MAPI-Funktionen verfügt (die gleichen Exporte wie die Mapi32.dll).
    
 _cchBufferSize_
  
> [in] Die Größe von  _szDllPath_ in Zeichen.
    
 _fInstall_
  
> [in] Weist die MAPI an, die private Mapi32.dll Komponente zu installieren, wenn sie nicht vorhanden ist.
    
## <a name="return-value"></a>Rückgabewert

 **STIMMT**
  
> Der Pfad wurde gefunden.
    
 **FALSE**
  
> Der Pfad wurde nicht gefunden.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **FGetComponentPath-Funktion,** wenn Sie den Pfad zum privaten Mapi32.dll abrufen müssen. 
  
## <a name="see-also"></a>Siehe auch



[Auswählen einer bestimmten Version der zu ladenden MAPI](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll Stub Registry Einstellungen](https://msdn.microsoft.com/library/dd162409.aspx)

