---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347747"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Offlineobjekt basierend auf einem bestimmten Profil.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32. dll  <br/> |
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
  
> in Dieser Parameter wird nicht verwendet. Es muss 0 sein.
    
 _pwszProfileNameIn_
  
> in Der Name des Profils, für das das Offlineobjekt gilt. Sie muss in Unicode ausgedrückt werden. 
    
 _pGUID_
  
> in Zeiger auf eine GUID, die verwendet werden kann, um dieses Objekt von anderen Offlineobjekten eindeutig zu identifizieren. Es muss **GUID_GlobalState**sein.
    
 _Beibehalten_
  
> in Dieser Parameter wird nicht verwendet. Sie muss **null**sein.
    
 _ppOfflineObj_
  
> Out Ein Zeiger auf das angeforderte Offlineobjekt. Der Aufrufer kann diesen Zeiger verwenden, um auf die [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) -Schnittstelle zuzugreifen, um die Rückrufe zu finden, die dieses Objekt unterstützt, und um Rückrufe dafür einzurichten. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
- Der Funktionsaufruf ist erfolgreich.
    
MAPI_E_NOT_FOUND
  
- Fehler beim Funktionsaufruf.
    
## <a name="remarks"></a>Bemerkungen

Dies ist der erste Aufruf eines Clients, wenn der Client über Verbindungsstatusänderungen für ein bestimmtes Profil benachrichtigt werden möchte. Beim Aufrufen von **HrOpenOfflineObj**ruft der Client ein Offlineobjekt ab, das **IMAPIOfflineMgr**unterstützt. Der Client kann die Rückruf Typen überprüfen, die vom Objekt unterstützt werden (mithilfe von [IMAPIOffline:: getCapabilities](imapioffline-getcapabilities.md)), und dann Rückrufe dafür einrichten (mithilfe von [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)).
  
Wenn Sie [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) verwenden, um nach der Adresse dieser Funktion in msmapi32. dll zu suchen, geben Sie **HrOpenOfflineObj @ 20** als Prozedurnamen an. 
  
 **HrOpenOfflineObj** funktioniert nur für Clients, die MAPI-Anbieter, COM-Add-Ins und Exchange-Client Erweiterungen sind, die innerhalb des Outlook-Prozesses ausgeführt werden. Andernfalls gibt **HrOpenOfflineObj** **MAPI_E_NOT_FOUND**zurück. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

