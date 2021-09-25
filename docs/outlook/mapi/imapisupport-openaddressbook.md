---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e23ff9bcf7ec5dafc32598690700a71f511fadef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567410"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf das Adressbuch.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll. Gültige Werte sind NULL, was die [IAddrBook-StandardaddrBook-Schnittstelle](iaddrbookimapiprop.md)und IID_IAddrBook angibt.
    
 _ulFlags_
  
> Reserviert; muss Null sein.
    
 _lppAdrBook_
  
> [out] Ein Zeiger auf einen Zeiger auf das Adressbuch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Zugriff auf das Adressbuch wurde bereitgestellt.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber mindestens ein Adressbuchanbieter konnte nicht geladen werden. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::OpenAddressBook-Methode** wird für alle Supportobjekte des Dienstanbieters implementiert. Dienstanbieter, in der Regel eng gekoppelte Nachrichtenspeicher- und Transportanbieter, rufen **OpenAddressBook** auf, um Zugriff auf das Adressbuch zu erhalten. Der **zurückgegebene IAddrBook-Zeiger** kann für eine Vielzahl von Adressbuchaufgaben verwendet werden, z. B. das Öffnen von Adressbuchcontainern, das Suchen von Messagingbenutzern und das Anzeigen von Adressdialogfeldern. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenAddressBook** kann MAPI_W_ERRORS_RETURNED zurückgeben, wenn es einen oder mehrere Adressbuchanbieter im aktuellen Profil nicht laden kann. Dieser Wert ist eine Warnung, und Sie sollten den Anruf als erfolgreich behandeln. Auch wenn alle Adressbuchanbieter nicht geladen werden konnten, ist **OpenAddressBook** weiterhin erfolgreich und gibt MAPI_W_ERRORS_RETURNED und einen **IAddrBook-Zeiger** im  _lppAdrBook-Parameter_ zurück. Da **OpenAddressBook** immer einen gültigen **IAddrBook-Zeiger** zurückgibt, müssen Sie ihn freigeben, wenn Sie ihn nicht mehr verwenden. 
  
Wenn ein oder mehrere Adressbuchanbieter nicht geladen werden konnten, rufen [Sie IMAPISupport::GetLastError](imapisupport-getlasterror.md) auf, um eine [MAPIERROR-Struktur](mapierror.md) abzurufen, die Informationen zu den Anbietern enthält, die nicht geladen wurden. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

