---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cf5060ba2113032fe1e13e5417590006808a53e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792760"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Betrifft**: Outlook 
  
Aktiviert oder deaktiviert eine Client-Standardprofil.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Profils, das werden die Standardeinstellung, oder NULL. _LpszProfileName_ bedeutet von NULL, dass **SetDefaultProfile** vorhandenen Standardprofils entfernen sollte den Client ohne Standardwert verlassen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolge steuert auf _LpszProfileName_zeigt. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Der Name der Benutzerprofildienst wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name der Benutzerprofildienst im ANSI-Format.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Ein Standardprofil wurde erfolgreich hergestellt oder entfernt.
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::SetDefaultProfile** -Methode stellt ein bestimmtes Profil als Standardprofil für den Client her, oder löscht den aktuellen Standardprofils. Das Standardprofil ist das Profil, das automatisch verwendet wird, wenn der Client eine MAPI-Sitzung beginnt. **SetDefaultProfile** wird auch neues Standardprofil **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))-Eigenschaft auf true festgelegt.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Sitzung mit dem Standardprofil starten möchten, übergeben Sie die Kennzeichen MAPI_USE_DEFAULT an die Funktion [MAPILogonEx](mapilogonex.md) . 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Kanonische PidTagDefaultProfile-Eigenschaft](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)

