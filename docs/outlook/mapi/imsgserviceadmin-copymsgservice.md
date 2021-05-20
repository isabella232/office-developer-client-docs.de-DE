---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432121"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert einen Nachrichtendienst in ein Profil. 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner des zu kopierenden Nachrichtendiensts enthält. 
    
 _lpszDisplayName_
  
> [in] Dieser Parameter ist veraltet. 
    
 _lpInterfaceToCopy_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt des zu kopierende Nachrichtendiensts verwendet werden soll. Das Übergeben von NULL führt zur Verwendung der Standardprofilabschnittsschnittstelle [IProfSect.](iprofsectimapiprop.md)
    
 _lpInterfaceDst_
  
> [in] Ein Zeiger auf die IID, die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, auf das der  _lpObjectDst-Parameter_ verweist. Übergeben von NULL-Ergebnissen in der Sitzungsschnittstelle [IMAPISession](imapisessioniunknown.md), die verwendet wird. Der  _lpInterfaceDst-Parameter_ kann auch auf IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Ein Zeiger auf einen Zeiger auf ein Sitzungs- oder Nachrichtendienstverwaltungsobjekt. Der Objekttyp sollte dem in _lpInterfaceDst übergebenen Schnittstellenbezeichner entsprechen._ Gültige Objektzeiger sind LPMAPISESSION und LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Nachrichtendienst kopiert wird. Die folgenden Kennzeichen können festgelegt werden:
    
SERVICE_UI_ALWAYS 
  
> Fordert an, dass der Nachrichtendienst immer ein Konfigurationseigenschaftsblatt zeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich kopiert.
    
MAPI_E_NO_ACCESS 
  
> Der Nachrichtendienst befindet sich bereits im Profil und lässt nicht mehrere Instanzen von sich selbst zu.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID,** auf die  _lpUID_ verweist, bezieht sich nicht auf einen vorhandenen Nachrichtendienst. 
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::CopyMsgService-Methode** kopiert einen Nachrichtendienst in ein Profil, entweder das aktive Profil oder ein anderes Profil. Das Profil, das den zu kopierende Nachrichtendienst und das Ziel enthält, muss nicht dasselbe Profil sein, aber es kann sein. 
  
Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht für einen Kopiervorgang aufgerufen. Der kopierte Nachrichtendienst verfügt über die gleichen Konfigurationseinstellungen wie der ursprüngliche. Um diese Einstellungen zu ändern, sollte ein Client die [IMsgServiceAdmin::ConfigureMsgService-Methode](imsgserviceadmin-configuremsgservice.md) aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

