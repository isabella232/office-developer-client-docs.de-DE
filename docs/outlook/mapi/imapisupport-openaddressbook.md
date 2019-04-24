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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329029"
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
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll. Gültige Werte sind NULL, womit die standardmäßige Adressbuch Schnittstelle [IAddrBook](iaddrbookimapiprop.md)und IID_IAddrBook angegeben wird.
    
 _ulFlags_
  
> Reserviert muss NULL sein.
    
 _lppAdrBook_
  
> Out Ein Zeiger auf einen Zeiger auf das Adressbuch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Zugriff auf das Adressbuch wurde bereitgestellt.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber mindestens ein Adressbuchanbieter konnte nicht geladen werden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: openaddressbook** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter, in der Regel eng gekoppelte Nachrichtenspeicher-und Transport **** Anbieter, rufen openaddressbook auf, um Zugriff auf das Adressbuch zu erhalten. Der zurückgegebene **IAddrBook** -Zeiger kann für eine Vielzahl von Adressbuch Aufgaben verwendet werden, einschließlich Öffnen von Adressbuch Containern, suchen nach Messaging Benutzern und Anzeigen von Adress Dialogfeldern. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **Openaddressbook** kann MAPI_W_ERRORS_RETURNED zurückgeben, wenn es einen oder mehrere der Adressbuchanbieter im aktuellen Profil nicht laden kann. Dieser Wert ist eine Warnung, und Sie sollten den Anruf als erfolgreich behandeln. Auch wenn alle Adressbuchanbieter nicht geladen werden konnten, ist **openaddressbook** weiterhin erfolgreich und gibt MAPI_W_ERRORS_RETURNED und einen **IAddrBook** -Zeiger im _lppAdrBook_ -Parameter zurück. Da **openaddressbook** immer einen gültigen **IAddrBook** -Zeiger zurückgibt, müssen Sie ihn freigeben, wenn Sie ihn nicht mehr verwenden. 
  
Wenn ein oder mehrere Adressbuchanbieter nicht geladen werden konnten, rufen Sie [IMAPISupport:: getlasterroraufzurufen](imapisupport-getlasterror.md) auf, um eine [MAPIERROR](mapierror.md) -Struktur abzurufen, die Informationen zu den Anbietern enthält, die nicht geladen wurden. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

