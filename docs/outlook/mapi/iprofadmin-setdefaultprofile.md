---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c59eb9a4972c72ae1afea4e21118df24eae756a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556315"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt das Standardprofil eines Clients fest oder löscht es.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Profils, der zum Standard wird, oder NULL. Wenn  _LpszProfileName_ auf NULL festgelegt wird, bedeutet dies, dass **SetDefaultProfile** das vorhandene Standardprofil entfernen sollte, sodass der Client nicht standardmäßig ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske von Flags, die den Typ der Zeichenfolge steuert, auf die mit  _lpszProfileName_ verwiesen wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Profilname hat das Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, hat der Profilname das ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Ein Standardprofil wurde erfolgreich erstellt oder entfernt.
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IProfAdmin::SetDefaultProfile-Methode** richtet entweder ein bestimmtes Profil als Standardprofil des Clients ein oder löscht das aktuelle Standardprofil. Das Standardprofil ist das Profil, das automatisch verwendet wird, wenn der Client eine MAPI-Sitzung startet. **SetDefaultProfile** legt auch die **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) -Eigenschaft des neuen Standardprofils auf TRUE fest.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Sitzung mit dem Standardprofil zu starten, übergeben Sie das flag MAPI_USE_DEFAULT an die [MAPILogonEx-Funktion.](mapilogonex.md) 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[PidTagDefaultProfile (kanonische Eigenschaft)](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

