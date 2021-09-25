---
title: Überwachen von Verbindungsstatusänderungen mithilfe eines Offlinestatus-Add-Ins
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f64f2ca3038053f008f29a811de3e4e6c82f53bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592032"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a>Überwachen von Verbindungsstatusänderungen mithilfe eines Offlinestatus-Add-Ins

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie ein Offlinestatus-Add-In zum Überwachen von Verbindungsstatusänderungen verwenden können, müssen Sie Funktionen zum Einrichten und Initialisieren des Add-Ins implementieren. Weitere Informationen finden Sie unter ["Einrichten eines Offlinestatus-Add-Ins".](setting-up-an-offline-state-add-in.md)
  
Nachdem Sie das Offlinestatus-Add-In eingerichtet haben, müssen Sie die **[HrOpenOfflineObj-Funktion](hropenofflineobj.md)** verwenden, um ein Offlineobjekt abzurufen. Mit diesem Offlineobjekt können Sie den Zustandsmonitor initialisieren und dann den aktuellen Status abrufen und festlegen. 
  
In diesem Thema werden diese Zustandsüberwachungsfunktionen anhand von Codebeispielen aus dem Beispiel-Offlinestatus-Add-In veranschaulicht. Das Offlinestatus-Beispiel-Add-In ist ein COM-Add-In, das Outlook ein **Offlinestatusmenü** hinzufügt und die Offlinestatus-API verwendet. Über das Menü **"Offlinestatus"** können Sie die Zustandsüberwachung aktivieren oder deaktivieren, den aktuellen Status überprüfen und den aktuellen Status ändern. Weitere Informationen zum Herunterladen und Installieren des Offlinestatus-Add-In-Beispiels finden Sie unter [Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md). Weitere Informationen zur Offlinestatus-API finden Sie unter [Informationen zur Offlinestatus-API](about-the-offline-state-api.md).
  
Wenn das Offlinestatus-Add-In getrennt wird, müssen Sie Funktionen implementieren, um das Add-In ordnungsgemäß zu beenden und zu bereinigen. Weitere Informationen finden Sie unter [Trennen eines Offlinestatus-Add-Ins.](disconnecting-an-offline-state-add-in.md)
  
## <a name="open-offline-object-routine"></a>Open Offline-Objektroutine

Damit der Client benachrichtigt wird, wenn eine Verbindungsstatusänderung auftritt, müssen Sie die **[HrOpenOfflineObj-Funktion](hropenofflineobj.md)** aufrufen. Diese Funktion öffnet ein Offlineobjekt, das **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** unterstützt. Die **HrOpenOfflineObj-Funktion** ist in der Headerdatei "ConnectionState.h" definiert. 
  
> [!NOTE]
> Die **HrOpenOfflineObj-Funktion** wird in der Headerdatei "ImportProcs.h" wie folgt deklariert:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;` . 
  
### <a name="hropenofflineobj-example"></a>HrOpenOfflineObj-Beispiel

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a>Initialisieren der Monitorroutine

Die  `InitMonitor` Funktion ruft die **HrOpenOfflineObj-Funktion** auf. Die `InitMonitor` Funktion ruft **CMyOfflineNotify** auf, damit Outlook Rückrufbenachrichtigungen an den Client senden können, und registriert den Rückruf über die **[variable MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** `AdviseInfo` .
  
### <a name="initmonitor-example"></a>Beispiel für InitMonitor()

```cpp
void InitMonitor(LPCWSTR szProfile) 
{ 
    if (!szProfile) return; 
    Log(true,_T("Initializing Outlook Offline State Monitor\n")); 
    HRESULT hRes = S_OK; 
 
    if (g_lpOfflineMgr) 
    { 
        Log(true,_T("Already initialized\n")); 
        return; 
    } 
     
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                ULONG ulCap = NULL; 
                hRes = lpOffline->GetCapabilities(&ulCap); 
                 
                if (ulCap & MAPIOFFLINE_CAPABILITY_OFFLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_OFFLINE supported\n")); 
                if (ulCap & MAPIOFFLINE_CAPABILITY_ONLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_ONLINE supported\n")); 
                 
                if (ulCap & (MAPIOFFLINE_CAPABILITY_OFFLINE | MAPIOFFLINE_CAPABILITY_ONLINE)) 
                { 
                    CMyOfflineNotify* lpImplNotify = new CMyOfflineNotify(); 
                     
                    if (lpImplNotify) 
                    { 
                        MAPIOFFLINE_ADVISEINFO AdviseInfo = {0}; 
                        AdviseInfo.ulSize = sizeof(MAPIOFFLINE_ADVISEINFO); 
                        AdviseInfo.ulClientToken = 0;// something you want to get handed back when you get the notification 
                        AdviseInfo.CallbackType = MAPIOFFLINE_CALLBACK_TYPE_NOTIFY; 
                        AdviseInfo.pCallback = lpImplNotify; 
                        AdviseInfo.ulAdviseTypes = MAPIOFFLINE_ADVISE_TYPE_STATECHANGE; 
                        AdviseInfo.ulStateMask = MAPIOFFLINE_STATE_ALL; 
                         
                        hRes = g_lpOfflineMgr->Advise(MAPIOFFLINE_ADVISE_DEFAULT, &AdviseInfo, &g_ulAdviseToken); 
                        Log(true,"ulAdviseToken = 0x%08X\n",g_ulAdviseToken); 
                    } 
                } 
                lpOffline->Release(); 
            }                 
        } 
    } 
}
```

## <a name="get-current-state-routine"></a>Abrufen der Routine für den aktuellen Status

Die  `GetCurrentState` Funktion ruft die **HrOpenOfflineObj-Funktion** auf und verwendet dann das Offlineobjekt, um den aktuellen Verbindungsstatus abzurufen. Der aktuelle Status wird in der  `ulCurState` Variablen zurückgegeben, die in der Funktion verwendet wird,  `CButtonEventHandler::Click` um dem Benutzer den aktuellen Status anzuzeigen. 
  
### <a name="getcurrentstate-example"></a>GetCurrentState() (Beispiel)

```cpp
ULONG (LPCWSTR szProfile) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Getting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
    ULONG ulCurState = NULL; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                hRes = lpOffline->GetCurrentState(&ulCurState); 
                Log(true,_T("GetCurrentState returned 0x%08X\n"),hRes); 
 
                switch(ulCurState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("Current state is 0x%0X\n"),ulCurState); 
                } 
                lpOffline->Release(); 
            } 
        } 
    } 
    return ulCurState; 
}
```

## <a name="set-current-state-routine"></a>Festlegen der Routine für den aktuellen Status

Die  `SetCurrentState` Funktion ruft die **HrOpenOfflineObj-Funktion** auf und verwendet dann das Offlineobjekt, um den aktuellen Verbindungsstatus festzulegen. Die  `CButtonEventHandler::Click` Funktion ruft die Funktion  `SetCurrentState` auf, und der neue Zustand wird über die  `ulState` Variable übergeben. 
  
### <a name="setcurrentstate-example"></a>SetCurrentState() (Beispiel)

```cpp
HRESULT SetCurrentState(LPCWSTR szProfile, ULONG ulFlags, ULONG ulState) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Setting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                switch(ulFlags) 
                { 
                case MAPIOFFLINE_FLAG_BLOCK: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_BLOCK\n")); 
                    break; 
                case MAPIOFFLINE_FLAG_DEFAULT: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_DEFAULT\n")); 
                    break; 
                default: 
                    Log(true,_T("Flag used: 0x%0X\n"),ulFlags); 
                } 
                switch(ulState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("New state will be 0x%0X\n"),ulState); 
                } 
                hRes = lpOffline->SetCurrentState(ulFlags, MAPIOFFLINE_STATE_OFFLINE_MASK,ulState,NULL); 
                Log(true,_T("SetCurrentState returned 0x%08X\n"),hRes); 
                 
                lpOffline->Release(); 
            } 
        } 
    } 
    return hRes; 
}
```

## <a name="notification-routine"></a>Benachrichtigungsroutine

Die **[IMAPIOfflineNotify::Notify-Funktion](imapiofflinenotify-notify.md)** wird von Outlook verwendet, um Benachrichtigungen an einen Client zu senden, wenn der Verbindungsstatus geändert wird. 
  
### <a name="cmyofflinenotifynotify-example"></a>CMyOfflineNotify::Notify()-Beispiel

```cpp
void CMyOfflineNotify::Notify(const MAPIOFFLINE_NOTIFY *pNotifyInfo) 
{ 
    Log(true,_T("CMyOfflineNotify::Notify\n")); 
    if    (pNotifyInfo == NULL) 
    {     
        Log(true,_T("pNotifyInfo is NULL\n")); 
    } 
    else 
    { 
        Log(true,_T("pNotifyInfo->ulSize == 0x%0X\n"),pNotifyInfo->ulSize); 
        switch(pNotifyInfo->NotifyType) 
        { 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->NotifyType == 0x%08X\n"),pNotifyInfo->NotifyType); 
        } 
        Log(true,_T("pNotifyInfo->ulClientToken == 0x%0X\n"),pNotifyInfo->ulClientToken); 
        switch(pNotifyInfo->Info.StateChange.ulMask) 
        { 
            case    MAPIOFFLINE_STATE_OFFLINE_MASK: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == MAPIOFFLINE_STATE_OFFLINE_MASK\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulMask); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateOld) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateOld); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateNew) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateNew); 
        } 
    } 
    return; 
}
```

## <a name="see-also"></a>Siehe auch

- [Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
- [Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md)
- [Informationen zum Offlinestatus-Add-In-Beispiel](about-the-sample-offline-state-add-in.md)
- [Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md)
- [Trennen eines Offlinestatus-Add-Ins](disconnecting-an-offline-state-add-in.md)

