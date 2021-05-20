---
title: Überwachen von Verbindungsstatusänderungen mithilfe eines Offlinestatus-Add-Ins
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d24a6d93943883a5503b57ef223d9be777af13d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431302"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a><span data-ttu-id="4ee98-103">Überwachen von Verbindungsstatusänderungen mithilfe eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="4ee98-103">Monitoring connection state changes using an offline state add-in</span></span>

<span data-ttu-id="4ee98-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ee98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ee98-105">Bevor Sie ein Offlinestatus-Add-In zum Überwachen von Verbindungsstatusänderungen verwenden können, müssen Sie Funktionen zum Einrichten und Initialisieren des Add-Ins implementieren.</span><span class="sxs-lookup"><span data-stu-id="4ee98-105">Before you can use an offline state add-in to monitor connection state changes, you must implement functions to set up and initialize the add-in.</span></span> <span data-ttu-id="4ee98-106">Weitere Informationen finden Sie unter [Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="4ee98-106">For more information, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="4ee98-107">Nachdem Sie das Offlinestatus-Add-In eingerichtet haben, müssen Sie die **[HrOpenOfflineObj-Funktion](hropenofflineobj.md)** verwenden, um ein Offlineobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ee98-107">After you set up the offline state add-in, you must use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object.</span></span> <span data-ttu-id="4ee98-108">Mit diesem Offlineobjekt können Sie den Statusmonitor initialisieren und dann den aktuellen Status erhalten und festlegen.</span><span class="sxs-lookup"><span data-stu-id="4ee98-108">Using this offline object, you can initialize your state monitor, and then get and set the current state.</span></span> 
  
<span data-ttu-id="4ee98-109">In diesem Thema werden diese Zustandsüberwachungsfunktionen anhand von Codebeispielen aus dem Beispiel-Offlinestatus-Add-In demonstriert.</span><span class="sxs-lookup"><span data-stu-id="4ee98-109">In this topic, these state monitoring functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="4ee98-110">Das Beispiel-Offlinestatus-Add-In ist ein COM-Add-In, das ein **Offlinestatusmenü** zu Outlook und die Offlinestatus-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ee98-110">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="4ee98-111">Über das **Menü Offlinestatus** können Sie die Zustandsüberwachung aktivieren oder deaktivieren, den aktuellen Status überprüfen und den aktuellen Status ändern.</span><span class="sxs-lookup"><span data-stu-id="4ee98-111">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="4ee98-112">Weitere Informationen zum Herunterladen und Installieren des Offlinestatus-Add-In-Beispiels finden Sie unter [Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="4ee98-112">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="4ee98-113">Weitere Informationen zur Offlinestatus-API finden Sie unter [Informationen zur Offlinestatus-API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="4ee98-113">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="4ee98-114">Wenn das Offlinestatus-Add-In getrennt wird, müssen Sie Funktionen implementieren, um das Add-In ordnungsgemäß zu beenden und zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="4ee98-114">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="4ee98-115">Weitere Informationen finden Sie unter [Disconnecting an Offline State Add-In](disconnecting-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="4ee98-115">For more information, see [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span></span>
  
## <a name="open-offline-object-routine"></a><span data-ttu-id="4ee98-116">Öffnen der Offlineobjektroutine</span><span class="sxs-lookup"><span data-stu-id="4ee98-116">Open Offline Object routine</span></span>

<span data-ttu-id="4ee98-117">Damit der Client benachrichtigt wird, wenn eine Verbindungsstatusänderung auftritt, müssen Sie die **[HrOpenOfflineObj-Funktion](hropenofflineobj.md)** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ee98-117">For the client to be notified when a connection state change occurs, you must call the **[HrOpenOfflineObj](hropenofflineobj.md)** function.</span></span> <span data-ttu-id="4ee98-118">Diese Funktion öffnet ein Offlineobjekt, das **[IMAPIOfflineMgr unterstützt.](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="4ee98-118">This function opens an offline object that supports **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> <span data-ttu-id="4ee98-119">Die **HrOpenOfflineObj-Funktion** ist in der ConnectionState.h-Headerdatei definiert.</span><span class="sxs-lookup"><span data-stu-id="4ee98-119">The **HrOpenOfflineObj** function is defined in the ConnectionState.h header file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4ee98-120">Die **HrOpenOfflineObj-Funktion** wird in der ImportProcs.h-Headerdatei wie folgt deklariert:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;` .</span><span class="sxs-lookup"><span data-stu-id="4ee98-120">The **HrOpenOfflineObj** function is declared in the ImportProcs.h header file as follows:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span></span> 
  
### <a name="hropenofflineobj-example"></a><span data-ttu-id="4ee98-121">Beispiel für HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="4ee98-121">HrOpenOfflineObj example</span></span>

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a><span data-ttu-id="4ee98-122">Initialisieren der Überwachungsroutine</span><span class="sxs-lookup"><span data-stu-id="4ee98-122">Initialize Monitor routine</span></span>

<span data-ttu-id="4ee98-123">Die  `InitMonitor` Funktion ruft die **HrOpenOfflineObj-Funktion** auf.</span><span class="sxs-lookup"><span data-stu-id="4ee98-123">The  `InitMonitor` function calls the **HrOpenOfflineObj** function.</span></span> <span data-ttu-id="4ee98-124">Die `InitMonitor` Funktion ruft **CMyOfflineNotify** auf, damit Outlook Rückrufbenachrichtigungen an den Client senden kann, und registriert den **[Rückruf](mapioffline_adviseinfo.md)** über die MAPIOFFLINE_ADVISEINFO Variable `AdviseInfo` .</span><span class="sxs-lookup"><span data-stu-id="4ee98-124">The  `InitMonitor` function calls **CMyOfflineNotify** so that Outlook can send callback notifications to the client, and registers the callback through the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** variable  `AdviseInfo`.</span></span>
  
### <a name="initmonitor-example"></a><span data-ttu-id="4ee98-125">Beispiel für InitMonitor()</span><span class="sxs-lookup"><span data-stu-id="4ee98-125">InitMonitor() example</span></span>

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

## <a name="get-current-state-routine"></a><span data-ttu-id="4ee98-126">Get Current State routine</span><span class="sxs-lookup"><span data-stu-id="4ee98-126">Get Current State routine</span></span>

<span data-ttu-id="4ee98-127">Die  `GetCurrentState` Funktion ruft die **HrOpenOfflineObj-Funktion** auf und verwendet dann das Offlineobjekt, um den aktuellen Verbindungsstatus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ee98-127">The  `GetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to get the current connection state.</span></span> <span data-ttu-id="4ee98-128">Der aktuelle Status wird in der Variablen zurückgegeben, die in der Funktion verwendet wird, um dem Benutzer den aktuellen Status  `ulCurState`  `CButtonEventHandler::Click` zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="4ee98-128">The current state is returned in the  `ulCurState` variable, which is used in the  `CButtonEventHandler::Click` function to display the current state to the user.</span></span> 
  
### <a name="getcurrentstate-example"></a><span data-ttu-id="4ee98-129">GetCurrentState()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ee98-129">GetCurrentState() example</span></span>

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

## <a name="set-current-state-routine"></a><span data-ttu-id="4ee98-130">Festlegen der Routine für den aktuellen Status</span><span class="sxs-lookup"><span data-stu-id="4ee98-130">Set Current State routine</span></span>

<span data-ttu-id="4ee98-131">Die  `SetCurrentState` Funktion ruft die **HrOpenOfflineObj-Funktion** auf und verwendet dann das Offlineobjekt, um den aktuellen Verbindungsstatus zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="4ee98-131">The  `SetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to set the current connection state.</span></span> <span data-ttu-id="4ee98-132">Die  `CButtonEventHandler::Click` Funktion ruft die Funktion  `SetCurrentState` auf, und der neue Zustand wird über die Variable  `ulState` übergeben.</span><span class="sxs-lookup"><span data-stu-id="4ee98-132">The  `CButtonEventHandler::Click` function calls the  `SetCurrentState` function and the new state is passed in through the  `ulState` variable.</span></span> 
  
### <a name="setcurrentstate-example"></a><span data-ttu-id="4ee98-133">SetCurrentState()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ee98-133">SetCurrentState() example</span></span>

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

## <a name="notification-routine"></a><span data-ttu-id="4ee98-134">Benachrichtigungsroutine</span><span class="sxs-lookup"><span data-stu-id="4ee98-134">Notification routine</span></span>

<span data-ttu-id="4ee98-135">Die **[IMAPIOfflineNotify::Notify-Funktion](imapiofflinenotify-notify.md)** wird von Outlook verwendet, um Benachrichtigungen an einen Client zu senden, wenn änderungen im Verbindungsstatus vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="4ee98-135">The **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** function is used by Outlook to send notifications to a client when there are changes in the connection state.</span></span> 
  
### <a name="cmyofflinenotifynotify-example"></a><span data-ttu-id="4ee98-136">CMyOfflineNotify::Notify()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ee98-136">CMyOfflineNotify::Notify() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="4ee98-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ee98-137">See also</span></span>

- [<span data-ttu-id="4ee98-138">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="4ee98-138">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="4ee98-139">Installieren des Offlinestatus-Add-In-Beispiels</span><span class="sxs-lookup"><span data-stu-id="4ee98-139">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="4ee98-140">Informationen zum Offlinestatus-Add-In-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ee98-140">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="4ee98-141">Einrichten eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="4ee98-141">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="4ee98-142">Trennen der Trennung eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="4ee98-142">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

