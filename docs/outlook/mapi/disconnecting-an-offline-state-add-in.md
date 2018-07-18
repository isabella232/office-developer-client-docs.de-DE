---
title: Trennen eines Offlinestatus-Add-Ins
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 82f529f58a62f412ed8b25d1ceaf508463491612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791542"
---
# <a name="disconnecting-an-offline-state-add-in"></a>Trennen eines Offlinestatus-Add-Ins

**Betrifft**: Outlook 
  
Wenn das Add-in offline-Status getrennt ist, müssen Sie implementieren Funktionen zum ordnungsgemäß beendet und bereinigen Sie das Add-in. Weitere Informationen zum Einrichten und im Offlinemodus state-add-in zum Überwachen von Änderungen am Status von Verbindung finden Sie unter [Einstellung von einer Offline-Status-Add-in](setting-up-an-offline-state-add-in.md) und [Monitoring Verbindung Zustand Änderungen mithilfe einer Offline-Status-Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
In diesem Thema, diese Trennung beenden und Bereinigungscode Funktionen werden mithilfe von Offline-Status Beispiel-Add-in Codebeispielen veranschaulicht. Das Beispiel Offline Zustand-Add-in ist ein COM-add-in, Outlook eine **Offline-Status** -Menü hinzugefügt und State-API verwendet. Über das Menü Offline-Status können Sie aktivieren oder Deaktivieren der Status der Überwachung, überprüfen Sie den aktuellen Status und ändern den aktuellen Status. Weitere Informationen zum Herunterladen und Installieren der Offline-Status Beispiel-Add-Ins finden Sie unter [Installieren der Offline-Status Beispiel-Add-Ins](installing-the-sample-offline-state-add-in.md). Weitere Informationen zur Status-API finden Sie unter [Über die Offline Zustand-API](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>Klicken Sie auf Trennen von Routine

Die **IDTExtensibility2.OnDisconnection** -Methode wird aufgerufen, wenn das Add-in Offline-Status entladen wird. Implementieren Sie Bereinigung von Code in dieser Funktion. Im folgenden Beispiel wird die Funktion **IDTExtensibility2.OnDisconnection** Ruft die `HrTermAddin` Funktion. 
  
### <a name="cmyaddinondisconnection-example"></a>CMyAddin::OnDisconnection()-Beispiel

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>Beenden Sie die Add-in-Funktion

Die `HrTermAddin` Funktionsaufrufe der `inDeInitMonitor`, `HrRemoveMenuItems`, und `UnloadLibraries` Funktionen zum Bereinigen des Status Offline-Add-Ins Fertig stellen. 
  
### <a name="cmyaddinhrtermaddin-example"></a>CMyAddin::HrTermAddin()-Beispiel

```cpp
HRESULT CMyAddin::HrTermAddin() 
{ 
    HRESULT hRes = S_OK; 
    DeInitMonitor(); 
    hRes =  HrRemoveMenuItems(); 
    UnloadLibraries(); 
    return hRes; 
}
```

## <a name="deinitialize-monitor-routine"></a>Monitor Routine deinitialize

Die `inDeInitMonitor` Funktion ruft die [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) -Funktion, um die Rückrufe für das offline-Objekt abzubrechen. 
  
### <a name="deinitmonitor-example"></a>DeInitMonitor()-Beispiel

```cpp
void DeInitMonitor() 
{ 
Log(true,_T("Deinitializing Outlook Offline State Monitor\n")); 
HRESULT hRes = S_OK; 
if (g_lpOfflineMgr) 
{ 
hRes = g_lpOfflineMgr->Unadvise(MAPIOFFLINE_UNADVISE_DEFAULT, g_ulAdviseToken); 
g_lpOfflineMgr->Release(); 
g_lpOfflineMgr = NULL; 
g_ulAdviseToken = NULL; 
} 
}
```

## <a name="remove-menu-items-routine"></a>Entfernen Sie im Menü Elemente Routine

Die `HrRemoveMenuItems` Funktionsaufrufe `DispEventUnadvise` für jedes Menüelement im, zeigen Sie im Menü **Offline-Status** und löscht dann das Menü **Status als offline anzeigen** . 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>CMyAddin::HrRemoveMenuItems()-Beispiel

```cpp
HRESULT CMyAddin::HrRemoveMenuItems() 
{     
    Log(true,"HrRemoveMenuItems\n"); 
    HRESULT hRes = S_OK; 
    if (m_fMenuItemsAdded) 
    { 
        try 
        { 
            if (m_spInitButton) 
            { 
                m_InitButtonHandler.DispEventUnadvise(m_spInitButton); 
            } 
            if (m_spDeinitButton) 
            { 
                m_DeinitButtonHandler.DispEventUnadvise(m_spDeinitButton); 
            } 
            if (m_spGetStateButton) 
            { 
                m_GetStateButtonHandler.DispEventUnadvise(m_spGetStateButton); 
            } 
            if (m_spSetStateButton) 
            { 
                m_SetStateButtonHandler.DispEventUnadvise(m_spSetStateButton); 
            } 
 
            m_spMyMenu->Delete(); 
        } 
        catch(_com_error) 
        { 
            hRes = E_FAIL; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            m_fMenuItemsAdded = false; 
        } 
    } 
    return hRes; 
}
```

## <a name="unload-libraries-routine"></a>Unload Bibliotheken Routine

Wenn das Add-In entladen aus Outlook, wird die `UnloadLibraries` Funktion entlädt das Dynamic Link Libraries (DLLs), die für das Add-in erforderlich. 
  
### <a name="unloadlibraries-example"></a>UnloadLibraries()-Beispiel

```cpp
void UnloadLibraries() 
{ 
    Log(true,_T("UnloadLibraries - freeing modules\n")); 
    pfnHrOpenOfflineObj = NULL; 
    pfnMAPIFreeBuffer = NULL; 
    if (hModMSMAPI) FreeLibrary(hModMSMAPI); 
    hModMSMAPI = NULL; 
    if (hModMAPI) FreeLibrary(hModMAPI); 
    hModMAPI = NULL; 
    if (hModMAPIStub) FreeLibrary(hModMAPIStub); 
    hModMAPIStub = NULL; 
}
```

## <a name="see-also"></a>Siehe auch

- [Informationen zu der Offlinestatus-API](about-the-offline-state-api.md)
- [Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md)
- [Informationen zum Offlinestatus-Add-In-Beispiel](about-the-sample-offline-state-add-in.md)
- [Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md)
- [Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

