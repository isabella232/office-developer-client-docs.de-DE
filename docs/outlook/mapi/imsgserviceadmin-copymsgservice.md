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
ms.openlocfilehash: 791dfe094aa0ff1aab656b56fbdf7d59e880b92e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593732"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Kopiert eine Message Service in einem Profil. 
  
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
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner des Diensts zum Kopieren von Nachricht enthält. 
    
 _lpszDisplayName_
  
> [in] Dieser Parameter ist veraltet. 
    
 _lpInterfaceToCopy_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt des Diensts zum Kopieren von Nachrichten verwendet werden. Bei Übergabe von NULL führt die Standardprofil Abschnitt-Schnittstelle, [IProfSect](iprofsectimapiprop.md), verwendet wird.
    
 _lpInterfaceDst_
  
> [in] Ein Zeiger auf die IID, die die Schnittstelle verwendet werden, um Zugriff auf das Objekt, durch den Parameter _LpObjectDst_ auf darstellt. Bei Übergabe von NULL führt die Sitzungsschnittstelle, [IMAPISession](imapisessioniunknown.md), verwendet wird. Der Parameter _LpInterfaceDst_ kann auch auf IID_IMsgServiceAdmin festgelegt werden. 
    
 _lpObjectDst_
  
> [in] Ein Zeiger auf einen Zeiger auf eine Sitzung oder einer Nachricht Service Administration-Objekt. Der Identifier übergebenen _LpInterfaceDst_sollte der Typ des Objekts entsprechen. Gültige Objektzeigern sind LPMAPISESSION und LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Nachrichtendienst kopiert wird. Die folgenden Kennzeichen können festgelegt werden:
    
SERVICE_UI_ALWAYS 
  
> Fordert, dass die Messagingdiensts immer eine Konfiguration Eigenschaftenfenster anzuzeigen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich kopiert.
    
MAPI_E_NO_ACCESS 
  
> Message-Dienst ist bereits im Profil und lässt nicht mehrere Instanzen von sich selbst.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID** auf das _LpUID_ bezieht sich nicht auf einem vorhandenen Meldung-Dienst. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::CopyMsgService** -Methode kopiert eine Message Service in einem Profil, das aktive Profil oder ein anderes Profil. Das Profil, das den Dienst zu kopierenden enthält, und das Ziel müssen nicht das gleiche Profil werden, aber sie werden können. 
  
Die Messagingdiensts Eintrag Point-Funktion ist nicht für einen Kopiervorgang aufgerufen. Die kopierten Messagingdiensts hat die gleiche Konfigurationseinstellungen als den ursprünglichen. Um diese Einstellungen zu ändern, sollte ein Client die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

