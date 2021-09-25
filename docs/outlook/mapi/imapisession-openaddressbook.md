---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c7344829c9d4478d098a79b15a0a8cff4824a404
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567515"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet das integrierte MAPI-Adressbuch und gibt einen [IAddrBook-Zeiger](iaddrbookimapiprop.md) für den weiteren Zugriff zurück. 
  
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
  
> [in] Ein Handle für das übergeordnete Fenster des allgemeinen Adressdialogfelds und anderer verwandter Anzeigen.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll. Wenn **NULL** übergeben wird, wird ein Zeiger auf die Standardschnittstelle des Adressbuchs zurückgegeben, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Öffnen des Adressbuchs steuert. Das folgende Kennzeichen kann festgelegt werden:
    
AB_NO_DIALOG 
  
> Unterdrückt die Anzeige von Dialogfeldern. Wenn das AB_NO_DIALOG Flag nicht festgelegt ist, können die Adressbuchanbieter, die zum integrierten Adressbuch beitragen, den Benutzer zur Eingabe der erforderlichen Informationen auffordern. 
    
 _lppAdrBook_
  
> [out] Ein Zeiger auf einen Zeiger auf das Adressbuch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Adressbuch wurde erfolgreich geöffnet.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber die Container eines oder mehrerer Adressbuchanbieter konnten nicht geöffnet werden. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::OpenAddressBook-Methode** öffnet das integrierte MAPI-Adressbuch, eine Sammlung der Container auf oberster Ebene aller Adressbuchanbieter im Profil. Der Zeiger, der im  _Parameter lppAdrBook_ zurückgegeben wird, bietet weiteren Zugriff auf den Inhalt des Adressbuchs. Auf diese Weise kann der Aufrufer Aufgaben ausführen, z. B. das Öffnen einzelner Container, das Suchen von Messagingbenutzern und das Anzeigen gängiger Adressdialogfelder. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenAddressBook** gibt MAPI_W_ERRORS_RETURNED zurück, wenn es einen oder mehrere Adressbuchanbieter im Profil nicht laden kann. Dieser Wert ist eine Warnung, kein Fehlerwert. behandeln Sie es wie S_OK. **OpenAddressBook** gibt immer einen gültigen Zeiger im  _lppAdrBook-Parameter_ zurück, unabhängig davon, wie viele der Adressbuchanbieter nicht geladen werden konnten. Daher müssen Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Adressbuchs zu einem bestimmten Zeitpunkt vor der Abmeldung aufrufen. 
  
Wenn **OpenAddressBook** MAPI_W_ERRORS_RETURNED zurückgibt, rufen [Sie IMAPISession::GetLastError](imapisession-getlasterror.md) auf, um eine [MAPIERROR-Struktur](mapierror.md) abzurufen, die Informationen zu den fehlerhaften Anbietern enthält. Es wird eine einzelne **MAPIERROR-Struktur** zurückgegeben, die Informationen enthält, die von allen Anbietern bereitgestellt werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI verwendet die **IMAPISession::OpenAddressBook-Methode,** um das integrierte Adressbuch abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

