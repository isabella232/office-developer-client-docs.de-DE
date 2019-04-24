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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270168"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt fest oder löscht das Standardprofil eines Clients.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> in Ein Zeiger auf den Namen des Profils, das zum Standardwert wird, oder NULL. Wenn _lpszProfileName_ auf NULL festgelegt wird, bedeutet dies, dass **SetDefaultProfile** das vorhandene Standardprofil entfernen sollte, sodass der Client keinen Standardwert aufweist. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der Zeichenfolge steuert, auf die von _lpszProfileName_verwiesen wird. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Profilname ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Profilname im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Ein Standardprofil wurde erfolgreich erstellt oder entfernt.
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IProfAdmin:: SetDefaultProfile** -Methode richtet entweder ein bestimmtes Profil als Standardprofil des Clients ein oder löscht das aktuelle Standardprofil. Das Standardprofil ist das Profil, das automatisch verwendet wird, wenn der Client eine MAPI-Sitzung startet. **SetDefaultProfile** legt auch die **PR_DEFAULT_PROFILE** ([pidtagdefaultprofile (](pidtagdefaultprofile-canonical-property.md))-Eigenschaft des neuen Standardprofils auf true fest.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie eine Sitzung mit dem Standardprofil starten möchten, müssen Sie das MAPI_USE_DEFAULT-Flag an die [MAPILogonEx](mapilogonex.md) -Funktion weiterleiten. 
  
## <a name="see-also"></a>Siehe auch



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Kanonische Pidtagdefaultprofile (-Eigenschaft](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

