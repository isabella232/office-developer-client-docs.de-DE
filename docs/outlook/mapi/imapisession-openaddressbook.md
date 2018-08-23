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
ms.openlocfilehash: 0902aeb71ed66381772a808d21d77edb7e0e2da8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589875"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Öffnet das MAPI-integrierte Adressbuch, einen [IAddrBook](iaddrbookimapiprop.md) Zeiger für den weiteren Zugriff zurückgibt. 
  
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
  
> [in] Ein Handle für das übergeordnete Fenster der Adresse Standarddialogfeld und anderer weiterführende zeigt.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle für das Adressbuch zugreifen zu verwendende darstellt. Übergeben von **null** gibt einen Zeiger auf das Adressbuch Standardschnittstelle, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die das Öffnen des Adressbuchs steuert. Das folgende Flag kann festgelegt werden:
    
AB_NO_DIALOG 
  
> Unterdrückt die Anzeige von Dialogfeldern. Wenn das Flag AB_NO_DIALOG nicht festgelegt ist, können die adressbuchanbietern implementierte, die auf die integrierte Adressbuch beitragen der Benutzer für alle erforderlichen Informationen aufgefordert. 
    
 _lppAdrBook_
  
> [out] Ein Zeiger auf einen Zeiger auf das Adressbuch.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Adressbuch wurde erfolgreich geöffnet.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber die Container für eine oder mehrere adressbuchanbietern implementierte konnte nicht geöffnet werden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::OpenAddressBook** -Methode öffnet das integrierte Adressbuch MAPI, eine Auflistung von Container der obersten Ebene aller von der adressbuchanbietern implementierte im Profil. Der Zeiger, der im Parameter _LppAdrBook_ zurückgegeben wird, bietet weitere Zugriff auf den Inhalt des Adressbuchs. Dadurch wird den Anrufer für Aufgaben wie öffnen einzelne Container, messaging Benutzer suchen und Anzeigen von Dialogfeldern für allgemeine Adresse. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenAddressBook** gibt MAPI_W_ERRORS_RETURNED zurück, wenn mindestens eines der adressbuchanbietern implementierte im Profil geladen werden kann. Dieser Wert ist eine Warnung, keinen Fehlerwert. Behandeln Sie es wie S_OK zurück. **OpenAddressBook** gibt immer einen gültigen Zeiger in der _LppAdrBook_ -Parameter, unabhängig davon, wie viele der Address Book Anbieter konnte nicht geladen werden. Aus diesem Grund müssen Sie zu einem bestimmten Zeitpunkt auch immer im Adressbuch [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, vor der Abmeldung. 
  
Wenn **OpenAddressBook** MAPI_W_ERRORS_RETURNED zurückgegeben wird, rufen Sie [IMAPISession::GetLastError](imapisession-getlasterror.md) um eine [MAPIERROR](mapierror.md) -Struktur zu erhalten, die Informationen zu den fehlerhaften Anbietern enthält. Eine einzelne **MAPIERROR** -Struktur zurückgegeben, die Informationen von alle Anbieter bereitgestellt wird, enthält. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::OpenAddressBook** -Methode, um die integrierten Adressbuch abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

