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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329421"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet das integrierte MAPI-Adressbuch und gibt einen [IAddrBook-Zeiger für](iaddrbookimapiprop.md) weiteren Zugriff zurück. 
  
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
  
> [in] Ein Handle zum übergeordneten Fenster des Dialogfelds allgemeine Adresse und andere zugehörige Displays.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll. Wenn **Null** übergeben wird, wird ein Zeiger auf die Standardschnittstelle des Adressbuchs, [IAddrBook : IMAPIProp , zurückgegeben.](iaddrbookimapiprop.md) 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Öffnen des Adressbuchs steuert. Das folgende Flag kann festgelegt werden:
    
AB_NO_DIALOG 
  
> Unterdrückt die Anzeige von Dialogfeldern. Wenn das AB_NO_DIALOG nicht festgelegt ist, können die Adressbuchanbieter, die zum integrierten Adressbuch beitragen, den Benutzer zur Eingabe der erforderlichen Informationen aufforderen. 
    
 _lppAdrBook_
  
> [out] Ein Zeiger auf einen Zeiger auf das Adressbuch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Adressbuch wurde erfolgreich geöffnet.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Anruf ist erfolgreich, aber die Container eines oder mehreren Adressbuchanbietern konnten nicht geöffnet werden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::OpenAddressBook-Methode** öffnet das integrierte MAPI-Adressbuch, eine Auflistung der Container auf oberster Ebene aller Adressbuchanbieter im Profil. Der zeiger, der im  _lppAdrBook-Parameter_ zurückgegeben wird, bietet weiteren Zugriff auf den Inhalt des Adressbuchs. Dadurch kann der Anrufer Aufgaben ausführen, z. B. das Öffnen einzelner Container, das Suchen von Messagingbenutzern und das Anzeigen von Allgemeinen Adressdialogfeldern. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenAddressBook** gibt MAPI_W_ERRORS_RETURNED zurück, wenn es einen oder mehrere Adressbuchanbieter nicht in das Profil laden kann. Dieser Wert ist eine Warnung und kein Fehlerwert. behandeln, wie Sie es S_OK. **OpenAddressBook** gibt immer einen gültigen Zeiger im  _lppAdrBook-Parameter_ zurück, unabhängig davon, wie viele Adressbuchanbieter nicht geladen wurden. Daher müssen Sie immer die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Adressbuchs an einem bestimmten Punkt aufrufen, bevor Sie sich abmelden. 
  
Wenn **OpenAddressBook** MAPI_W_ERRORS_RETURNED, rufen Sie [IMAPISession::GetLastError](imapisession-getlasterror.md) auf, um eine [MAPIERROR-Struktur](mapierror.md) zu erhalten, die Informationen zu den fehlerhaften Anbietern enthält. Es wird **eine einzelne MAPIERROR-Struktur** zurückgegeben, die Informationen enthält, die von allen Anbietern bereitgestellt werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI verwendet die **IMAPISession::OpenAddressBook-Methode,** um das integrierte Adressbuch zu erhalten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

