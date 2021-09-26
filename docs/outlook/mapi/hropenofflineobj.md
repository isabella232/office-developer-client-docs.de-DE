---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 89b9f53c6677b61c9e61ae6cb77fe6451e786e85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610783"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Offlineobjekt basierend auf einem bestimmten Profil.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a>Parameter

 _ulReserved_
  
> [in] Dieser Parameter wird nicht verwendet. Es muss 0 sein.
    
 _pwszProfileNameIn_
  
> [in] Der Name des Profils, für das das Offlineobjekt verwendet wird. Sie muss in Unicode ausgedrückt werden. 
    
 _pGUID_
  
> [in] Zeiger auf eine GUID, die verwendet werden kann, um dieses Objekt aus anderen Offlineobjekten eindeutig zu identifizieren. Es muss **GUID_GlobalState** sein.
    
 _Erhalten_
  
> [in] Dieser Parameter wird nicht verwendet. Es muss **NULL** sein.
    
 _ppOfflineObj_
  
> [out] Ein Zeiger auf das angeforderte Offlineobjekt. Der Aufrufer kann diesen Zeiger verwenden, um auf die [IMAPIOfflineMgr : IMAPIOffline-Schnittstelle](imapiofflinemgrimapioffline.md) zuzugreifen, um die von diesem Objekt unterstützten Rückrufe zu finden und Rückrufe dafür einzurichten. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
- Der Funktionsaufruf ist erfolgreich.
    
MAPI_E_NOT_FOUND
  
- Der Funktionsaufruf ist fehlgeschlagen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Dies ist der erste Aufruf, den ein Client vornimmt, wenn der Client über Verbindungsstatusänderungen für ein bestimmtes Profil benachrichtigt werden möchte. Beim Aufrufen **von HrOpenOfflineObj** ruft der Client ein Offlineobjekt ab, das **IMAPIOfflineMgr** unterstützt. Der Client kann überprüfen, welche Arten von Rückrufen vom Objekt unterstützt werden (mithilfe von [IMAPIOffline::GetCapabilities),](imapioffline-getcapabilities.md)und dann Rückrufe dafür einrichten (mithilfe von [IMAPIOfflineMgr::Advise).](imapiofflinemgr-advise.md)
  
Wenn [Sie GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) zum Suchen nach der Adresse dieser Funktion in msmapi32.dll verwenden, geben Sie **HrOpenOfflineObj@20** als Prozedurnamen an. 
  
 **HrOpenOfflineObj** funktioniert nur für Clients, die MAPI-Anbieter, COM-Add-Ins und Exchange Clienterweiterungen sind, die innerhalb des Outlook-Prozesses ausgeführt werden. Andernfalls gibt **HrOpenOfflineObj** **MAPI_E_NOT_FOUND** zurück. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

