---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329421"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet das integrierte MAPI-Adressbuch und gibt einen [IAddrBook](iaddrbookimapiprop.md) -Zeiger für den weiteren Zugriff zurück. 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster des Dialogfelds "allgemeine Adresse" und andere zugehörige anzeigen.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll. Beim Übergeben von **null** wird ein Zeiger auf die Standardschnittstelle des Adressbuchs [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)zurückgegeben. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Öffnen des Adressbuchs steuert. Das folgende Flag kann festgelegt werden:
    
AB_NO_DIALOG 
  
> Unterdrückt die Anzeige von Dialogfeldern. Wenn das AB_NO_DIALOG-Flag nicht festgelegt ist, können die Adressbuchanbieter, die zum integrierten Adressbuch beitragen, den Benutzer um erforderliche Informationen auffordern. 
    
 _lppAdrBook_
  
> Out Ein Zeiger auf einen Zeiger auf das Adressbuch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Adressbuch wurde erfolgreich geöffnet.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber die Container eines oder mehrerer Adressbuchanbieter konnten nicht geöffnet werden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession:: openaddressbook** -Methode öffnet das integrierte MAPI-Adressbuch, eine Sammlung der Container der obersten Ebene aller Adressbuchanbieter im Profil. Der im Parameter _lppAdrBook_ zurückgegebene Zeiger bietet weiteren Zugriff auf den Inhalt des Adressbuchs. Dadurch kann der Anrufer Aufgaben wie das Öffnen einzelner Container, das Auffinden von Messaging Benutzern und das Anzeigen allgemeiner Adress Dialogfelder ausführen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **Openaddressbook** gibt MAPI_W_ERRORS_RETURNED zurück, wenn ein oder mehrere Adressbuchanbieter im Profil nicht geladen werden können. Dieser Wert ist eine Warnung, kein Fehlerwert; behandeln Sie Sie wie S_OK. **Openaddressbook** gibt immer einen gültigen Zeiger im _lppAdrBook_ -Parameter zurück, unabhängig davon, wie viele Adressbuchanbieter nicht geladen wurden. Daher müssen Sie vor dem Abmelden immer die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode des Adressbuchs aufrufen. 
  
Wenn **Openaddressbook** MAPI_W_ERRORS_RETURNED zurückgibt, rufen Sie [IMAPISession:: getlasterroraufzurufen](imapisession-getlasterror.md) auf, um eine [MAPIERROR](mapierror.md) -Struktur abzurufen, die Informationen zu den fehlerhaften Anbietern enthält. Es wird eine einzelne **MAPIERROR** -Struktur zurückgegeben, die von allen Anbietern bereitgestellte Informationen enthält. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: GetAddrBook  <br/> |MFCMAPI verwendet die **IMAPISession:: openaddressbook** -Methode, um das integrierte Adressbuch abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

