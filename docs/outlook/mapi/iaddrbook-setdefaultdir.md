---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6a74b10167506251160d508418a8894b8b7e3c6d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576142"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Richtet den angegebenen Container als Standardadressbuchcontainer ein.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Standardadressbuchcontainers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Standardadressbuchcontainer wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients und Dienstanbieter rufen die **SetDefaultDir-Methode** auf, um einen neuen Standardadressbuchcontainer einzurichten. Der Standardcontainer ist der Container, der dem Benutzer beim ersten Öffnen des Adressbuchs im Adressbuch angezeigt wird. **SetDefaultDir** speichert den Standardcontainer als Eintrag im Profil. Der Container bleibt als Standard, bis entweder ein weiterer Aufruf von **SetDefaultDir** in derselben Sitzung oder in einer anderen Sitzung erfolgt oder der Container entfernt wird. 
  
> [!NOTE]
> Die [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY-Eigenschaft](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) entspricht der Einstellung **"Automatisch auswählen"** im Dialogfeld "Adressbuchoptionen". Wenn diese Eigenschaft im [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) Profilabschnitt vorhanden ist und auf **"true"** festgelegt ist, wird im Adressbuchdialogfeld nicht mehr standardmäßig der von **SetDefaultDir** angegebene Container verwendet, sondern ein Adressbuch ausgewählt, das Microsoft Outlook für den Kontext, in dem das Dialogfeld angezeigt wurde, als geeignet ansieht. Beachten Sie, dass dies zu einer schlechten Erfahrung für Adressbuchanbieter von Drittanbietern führen kann. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI verwendet die **SetDefaultDir-Methode,** um den angegebenen Adressbuchcontainer als Standardcontainer festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

