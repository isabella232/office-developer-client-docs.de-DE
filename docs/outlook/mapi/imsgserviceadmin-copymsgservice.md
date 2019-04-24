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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309968"
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
  
> in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner des zu kopierende Nachrichtendiensts enthält. 
    
 _lpszDisplayName_
  
> in Dieser Parameter ist veraltet. 
    
 _lpInterfaceToCopy_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den Profil Abschnitt des Nachrichtendiensts zum Kopieren verwendet werden soll. Übergeben von NULL-Ergebnissen in der Standardprofil-Schnittstelle, [IProfSect](iprofsectimapiprop.md), wird verwendet.
    
 _lpInterfaceDst_
  
> in Ein Zeiger auf die IID, die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, auf das durch den _lpObjectDst_ -Parameter verwiesen wird. Übergeben von NULL-Ergebnissen in der Sitzungs Schnittstelle, [IMAPISession](imapisessioniunknown.md), wird verwendet. Der _lpInterfaceDst_ -Parameter kann auch auf IID_IMsgServiceAdmin festgelegt werden. 
    
 _lpObjectDst_
  
> in Ein Zeiger auf einen Zeiger auf ein Sitzungs-oder Nachrichtendienst-Verwaltungsobjekt. Der Objekttyp sollte der Schnittstellenkennung entsprechen, die in _lpInterfaceDst_übergeben wurde. Gültige Objektzeiger sind LPMAPISESSION und LPSERVICEADMIN.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie der Nachrichtendienst kopiert wird. Die folgenden Flags können festgelegt werden:
    
SERVICE_UI_ALWAYS 
  
> Fordert, dass der Nachrichtendienst immer ein Konfigurationseigenschaften Blatt anzeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich kopiert.
    
MAPI_E_NO_ACCESS 
  
> Der Nachrichtendienst befindet sich bereits im Profil und lässt keine mehrere Instanzen von sich selbst zu.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID** , auf die durch _lpUID_ verwiesen wird, bezieht sich nicht auf einen vorhandenen Nachrichtendienst. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin:: CopyMsgService** -Methode kopiert einen Nachrichtendienst in ein Profil, entweder das aktive Profil oder ein anderes Profil. Das Profil, das den zu kopierenden Nachrichtendienst enthält, und das Ziel muss nicht dasselbe Profil aufweisen, aber möglicherweise nicht. 
  
Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht für einen Kopiervorgang aufgerufen. Der kopierte Nachrichtendienst hat die gleichen Konfigurationseinstellungen wie sein ursprüngliches. Um diese Einstellungen zu ändern, sollte ein Client die [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

