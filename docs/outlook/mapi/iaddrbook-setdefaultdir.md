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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792002"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Betrifft**: Outlook 
  
Stellt den angegebenen Container als Standard Adressbuchcontainer her.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID der Standard-Adressbuchcontainer.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Standard-Adressbuchcontainer wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen Sie die **SetDefaultDir** -Methode, um eine neue Standard Adressbuchcontainer herzustellen. Der standardmäßige Container ist der Container, den der Benutzer erhält im Adressbuch angezeigt wird, wenn das Adressbuch zum ersten Mal geöffnet wird. **SetDefaultDir** speichert den Standardcontainer als Eintrag im Profil. Der Container bleibt unverändert bis einen weiteren Anruf zu **SetDefaultDir** in der gleichen Sitzung oder in einer anderen Sitzung erfolgt oder der Container wird entfernt. 
  
> [!NOTE]
> Die [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) -Eigenschaft entspricht der Einstellung **automatisch wählen Sie** im Dialogfeld Optionen für das Adressbuch. Wenn diese Eigenschaft im Abschnitt [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) Profile vorhanden ist und auf **true**festgelegt ist, im Adressbuch-Dialogfeld nicht mehr standardmäßig durch **SetDefaultDir**angegebene Container, jedoch wählt ein Adressbuch, von denen Microsoft Outlook annimmt. geeignet für den Kontext, in dem das Dialogfeld angezeigt wurde. Beachten Sie, dass dies eine schlechte Erfahrung für Drittanbieter-adressbuchanbietern implementierte führen kann. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI (engl.) verwendet die **SetDefaultDir** -Methode zum angegebenen Adressbuchcontainer eines machen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

