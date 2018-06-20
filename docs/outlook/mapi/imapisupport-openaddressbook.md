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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9cd1c7ce0983a47311b2626cc3b40b47748b951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792397"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle für das Adressbuch zugreifen zu verwendende darstellt. Gültige Werte sind NULL-Wert, womit die standard-Adresse Adressbuch-Schnittstelle [IAddrBook](iaddrbookimapiprop.md)und IID_IAddrBook.
    
 _ulFlags_
  
> Reserviert. NULL muss sein.
    
 _lppAdrBook_
  
> [out] Ein Zeiger auf einen Zeiger auf das Adressbuch.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Zugriff auf das Adressbuch wurde bereitgestellt.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber eine oder mehrere adressbuchanbietern implementierte konnte nicht geladen werden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::OpenAddressBook** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter, die in der Regel eng gekoppelten Nachricht speichern und transport-Anbieter, rufen Sie **OpenAddressBook** , um auf das Adressbuch zuzugreifen. Der zurückgegebene **IAddrBook** Zeiger kann für eine Vielzahl von Address Book Aufgaben, einschließlich Adresse Adressbuch-Containern und Suchen von messaging-Benutzer und Anzeige von Adresse Dialogfelder Öffnen verwendet werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenAddressBook** können MAPI_W_ERRORS_RETURNED zurückgeben, wenn mindestens eines der adressbuchanbietern implementierte im aktuellen Profil geladen werden kann. Dieser Wert ist eine Warnung und sollten Sie den Anruf als erfolgreich behandeln. Auch wenn alle Address Book Anbieter konnte nicht geladen werden, **OpenAddressBook** weiterhin erfolgreich ist, wird MAPI_W_ERRORS_RETURNED und einen **IAddrBook** Zeiger im Parameter _LppAdrBook_ zurückgeben. Da **OpenAddressBook** immer einen gültigen **IAddrBook** Zeiger zurückgibt, müssen Sie es Sie abschließend Verwendung freigeben. 
  
Wenn eine oder mehrere adressbuchanbietern implementierte konnte nicht geladen werden, rufen Sie [IMAPISupport::GetLastError](imapisupport-getlasterror.md) um eine [MAPIERROR](mapierror.md) -Struktur zu erhalten, die Informationen zu den Anbietern enthält, die nicht geladen wurden. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

