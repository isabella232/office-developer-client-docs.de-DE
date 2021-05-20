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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439625"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt das Standardprofil eines Clients fest oder deaktiviert es.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Profils, das zur Standardeinstellung wird, oder NULL. Das  _Festlegen von lpszProfileName_ auf NULL gibt an, dass **SetDefaultProfile** das vorhandene Standardprofil entfernen soll, ohne dass der Client einen Standardwert hat. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der Zeichenfolge steuert, auf die _von lpszProfileName verwiesen wird._ Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Profilname ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich der Profilname im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Ein Standardprofil wurde erfolgreich eingerichtet oder entfernt.
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::SetDefaultProfile-Methode** richtet entweder ein bestimmtes Profil als Standardprofil des Clients ein oder deaktiviert das aktuelle Standardprofil. Das Standardprofil ist das Profil, das automatisch verwendet wird, wenn der Client eine MAPI-Sitzung beginnt. **SetDefaultProfile** legt außerdem die Eigenschaft **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) des neuen Standardprofils auf TRUE fest.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Sitzung mit dem Standardprofil zu starten, übergeben Sie das MAPI_USE_DEFAULT an die [MAPILogonEx-Funktion.](mapilogonex.md) 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[PidTagDefaultProfile (kanonische Eigenschaft)](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

