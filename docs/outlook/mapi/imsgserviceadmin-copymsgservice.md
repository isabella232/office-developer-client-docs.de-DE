---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 95a361a44d4714365b9d8b379a0d7f1cb3f85f27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571689"
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
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt des zu kopierenden Nachrichtendiensts verwendet werden soll. Das Übergeben von NULL führt dazu, dass die standardmäßige Profilabschnittsschnittstelle [IProfSect](iprofsectimapiprop.md)verwendet wird.
    
 _lpInterfaceDst_
  
> [in] Ein Zeiger auf die IID, die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, auf das durch den  _lpObjectDst-Parameter_ verwiesen wird. Übergeben von NULL-Ergebnissen in der Sitzungsschnittstelle, [IMAPISession,](imapisessioniunknown.md)wird verwendet. Der  _Parameter lpInterfaceDst_ kann auch auf IID_IMsgServiceAdmin festgelegt werden. 
    
 _lpObjectDst_
  
> [in] Ein Zeiger auf einen Zeiger auf ein Sitzungs- oder Nachrichtendienst-Verwaltungsobjekt. Der Objekttyp sollte dem Schnittstellenbezeichner entsprechen, der in  _lpInterfaceDst_ übergeben wird. Gültige Objektzeiger sind LPMAPISESSION und LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Nachrichtendienst kopiert wird. Die folgenden Flags können festgelegt werden:
    
SERVICE_UI_ALWAYS 
  
> Fordert an, dass der Nachrichtendienst immer ein Konfigurationseigenschaftenblatt anzeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich kopiert.
    
MAPI_E_NO_ACCESS 
  
> Der Nachrichtendienst befindet sich bereits im Profil und lässt nicht mehrere Instanzen von sich selbst zu.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID,** auf die von  _lpUID_ verwiesen wird, bezieht sich nicht auf einen vorhandenen Nachrichtendienst. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::CopyMsgService-Methode** kopiert einen Nachrichtendienst in ein Profil, entweder das aktive Profil oder ein anderes Profil. Das Profil, das den zu kopierenden Nachrichtendienst enthält, und das Ziel muss nicht dasselbe Profil sein, kann aber sein. 
  
Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht für einen Kopiervorgang aufgerufen. Der kopierte Nachrichtendienst verfügt über die gleichen Konfigurationseinstellungen wie der ursprüngliche Nachrichtendienst. Um diese Einstellungen zu ändern, sollte ein Client die [IMsgServiceAdmin::ConfigureMsgService-Methode](imsgserviceadmin-configuremsgservice.md) aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

