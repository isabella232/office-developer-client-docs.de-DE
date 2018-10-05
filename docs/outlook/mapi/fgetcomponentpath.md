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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384500"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Pfad zu der privaten Mapi32.dll zurück.
  
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
  
> [in] Die MSIComponentID-Registrierungsschlüssel in [Mapi32.dll Stub Registrierungseinstellungen](https://msdn.microsoft.com/library/dd162409.aspx)beschrieben.
    
 _szQualifier_
  
> [in] Die MSIApplicationLCID oder MSIOfficeLCID Unterschlüssel in [Wählen Sie eine bestimmte Version von MAPI auf Load](how-to-choose-a-specific-version-of-mapi-to-load.md)beschrieben. Anrufer können **null** übergeben, wenn kein Qualifizierer vorhanden ist. 
    
 _szDllPath_
  
> [in] Der Pfad zu der privaten Mapi32.dll, die vollständigen MAPI-Funktionalität (die gleichen Exporte als die Mapi32.dll) hat.
    
 _cchBufferSize_
  
> [in] Die Größe des _SzDllPath_in Zeichen.
    
 _fInstall_
  
> [in] Erfahren Sie mehr MAPI, um die private Mapi32.dll Komponente zu installieren, wenn es nicht vorhanden ist.
    
## <a name="return-value"></a>Rückgabewert

 **"true"**
  
> Der Pfad wurde gefunden.
    
 **false**
  
> Der Pfad wurde nicht gefunden.
    
## <a name="remarks"></a>Hinweise

Verwenden Sie die **FGetComponentPath** -Funktion, wenn Sie den Pfad der privaten Mapi32.dll abzurufen müssen. 
  
## <a name="see-also"></a>Siehe auch



[Auswählen einer bestimmten zu ladenden MAPI-Version](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll Stub Registrierungseinstellungen](https://msdn.microsoft.com/library/dd162409.aspx)

