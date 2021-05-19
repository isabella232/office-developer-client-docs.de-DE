---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416881"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf das Adressbuch.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll. Gültige Werte sind NULL, was die Standardmäßige Adressbuchschnittstelle [IAddrBook](iaddrbookimapiprop.md)angibt, und IID_IAddrBook.
    
 _ulFlags_
  
> Reserviert; muss null sein.
    
 _lppAdrBook_
  
> [out] Ein Zeiger auf einen Zeiger auf das Adressbuch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Zugriff auf das Adressbuch wurde bereitgestellt.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Anruf war erfolgreich, aber mindestens ein Adressbuchanbieter konnte nicht geladen werden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::OpenAddressBook-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter, in der Regel eng gekoppelte Nachrichtenspeicher- und Transportanbieter, rufen **OpenAddressBook** auf, um Zugriff auf das Adressbuch zu erhalten. Der zurückgegebene **IAddrBook-Zeiger** kann für eine Vielzahl von Adressbuchaufgaben verwendet werden, z. B. das Öffnen von Adressbuchcontainern, das Suchen von Messagingbenutzern und das Anzeigen von Adressdialogfeldern. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenAddressBook** kann MAPI_W_ERRORS_RETURNED zurückgeben, wenn es einen oder mehrere Adressbuchanbieter im aktuellen Profil nicht laden kann. Dieser Wert ist eine Warnung, und Sie sollten den Anruf als erfolgreich behandeln. Auch wenn alle Adressbuchanbieter nicht geladen werden konnten, ist **OpenAddressBook** weiterhin erfolgreich und gibt MAPI_W_ERRORS_RETURNED und einen **IAddrBook-Zeiger** im  _lppAdrBook-Parameter_ zurück. Da **OpenAddressBook** immer einen gültigen **IAddrBook-Zeiger** zurückgibt, müssen Sie ihn los, sobald Sie mit der Verwendung fertig sind. 
  
Wenn ein oder mehrere Adressbuchanbieter nicht geladen werden konnten, rufen Sie [IMAPISupport::GetLastError](imapisupport-getlasterror.md) auf, um eine [MAPIERROR-Struktur](mapierror.md) zu erhalten, die Informationen zu den Anbietern enthält, die nicht geladen wurden. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

