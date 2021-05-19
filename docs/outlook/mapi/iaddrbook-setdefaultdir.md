---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341699"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Richtet den angegebenen Container als Standard-Adressbuchcontainer ein.
  
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
  
> [in] Ein Zeiger auf die Eintrags-ID des Standard-Adressbuchcontainers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Standard-Adressbuchcontainer wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen die **SetDefaultDir-Methode** auf, um einen neuen Standard-Adressbuchcontainer zu erstellen. Der Standardcontainer ist der Container, den der Benutzer beim ersten Öffnen des Adressbuchs im Adressbuch angezeigt sieht. **SetDefaultDir** speichert den Standardcontainer als Eintrag im Profil. Der Container bleibt die Standardeinstellung, bis ein anderer Aufruf von **SetDefaultDir** in derselben Sitzung oder in einer anderen Sitzung erfolgt oder der Container entfernt wird. 
  
> [!NOTE]
> Die [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) entspricht der Einstellung **Automatisch** auswählen im Dialogfeld Adressbuchoptionen. Wenn diese Eigenschaft im Abschnitt [IID_CAPONE_PROF-Profil](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) vorhanden ist und auf **true** festgelegt ist, wird im Adressbuchdialogfeld nicht mehr standardmäßig der von **SetDefaultDir** angegebene Container verwendet, sondern ein Adressbuch ausgewählt, das von Microsoft Outlook für den Kontext geeignet erachtet wird, in dem das Dialogfeld angezeigt wurde. Beachten Sie, dass dies zu einer schlechten Erfahrung für Adressbuchanbieter von Drittanbietern führen kann. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI verwendet die **SetDefaultDir-Methode,** um den angegebenen Adressbuchcontainer zum Standardcontainer zu machen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

