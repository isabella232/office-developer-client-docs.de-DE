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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Standardadressbuch-Adressbuch Containers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der standardmäßige Adressbuchcontainer wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen die **SetDefaultDir** -Methode auf, um einen neuen Standard Adressbuchcontainer einzurichten. Der Standardcontainer ist der Container, den der Benutzer im Adressbuch angezeigt sieht, wenn das Adressbuch zum ersten Mal geöffnet wird. **SetDefaultDir** speichert den Standardcontainer als Eintrag im Profil. Der Container bleibt als Standard, bis ein anderer Aufruf von **SetDefaultDir** in derselben Sitzung oder in einer anderen Sitzung erfolgt, oder der Container wird entfernt. 
  
> [!NOTE]
> Die [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) -Eigenschaft entspricht der Einstellung **automatisch auswählen** im Dialogfeld Adressbuchoptionen. Wenn diese Eigenschaft im Abschnitt [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) vorhanden ist und auf **true**festgelegt ist, ist das Adressbuch-Dialogfeld nicht mehr standardmäßig der Container von **SetDefaultDir**angegeben, aber wählt ein Adressbuch, das Microsoft Outlook berücksichtigt passend für den Kontext, in dem das Dialogfeld angezeigt wurde. Beachten Sie, dass dies zu einer schlechten Erfahrung für Drittanbieter-Adressbuchanbieter führen kann. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Abcontdlg. cpp  <br/> |CAbContDlg:: OnSetDefaultDir  <br/> |MFCMAPI verwendet die **SetDefaultDir** -Methode, um den angegebenen Adressbuchcontainer als Standard zu verwenden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

