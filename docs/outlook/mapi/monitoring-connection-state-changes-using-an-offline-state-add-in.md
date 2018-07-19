---
title: Überwachen von Änderungen am Status von Verbindung mit einer offline-Status-add-in
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f7f3bc0e305fb5aa7d6ae1e1909b573b3376ef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793266"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a><span data-ttu-id="83e09-103">Überwachen von Änderungen am Status von Verbindung mit einer offline-Status-add-in</span><span class="sxs-lookup"><span data-stu-id="83e09-103">Monitoring connection state changes using an offline state add-in</span></span>

<span data-ttu-id="83e09-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83e09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83e09-105">Bevor Sie zum Überwachen von Änderungen am Status der Verbindung eine offline-Status-Add-in verwenden können, müssen Sie die Funktionen zum Einrichten und initialisieren Sie das Add-in implementieren.</span><span class="sxs-lookup"><span data-stu-id="83e09-105">Before you can use an offline state add-in to monitor connection state changes, you must implement functions to set up and initialize the add-in.</span></span> <span data-ttu-id="83e09-106">Weitere Informationen finden Sie unter [Einstellung Up eine Offline-Status-Add-in](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="83e09-106">For more information, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="83e09-107">Nach dem Einrichten des offline-Status-add-Ins, müssen Sie die **[HrOpenOfflineObj](hropenofflineobj.md)** -Funktion verwenden, um eine offline-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="83e09-107">After you set up the offline state add-in, you must use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object.</span></span> <span data-ttu-id="83e09-108">Verwenden diese offline-Objekts, können Sie Ihren Monitor Zustand initialisieren und dann abrufen und Festlegen des aktuellen Zustands.</span><span class="sxs-lookup"><span data-stu-id="83e09-108">Using this offline object, you can initialize your state monitor, and then get and set the current state.</span></span> 
  
<span data-ttu-id="83e09-109">In diesem Thema werden die folgenden Überwachungsfunktionen Status mithilfe der Offline-Status Beispiel-Add-in Codebeispielen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="83e09-109">In this topic, these state monitoring functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="83e09-110">Das Offline-Status Beispiel-Add-in ist ein COM-add-in, die ein Menü **Status als offline anzeigen** zu Outlook hinzugefügt und State-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="83e09-110">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="83e09-111">Über das Menü **Offline-Status** können Sie aktivieren oder Deaktivieren der Status der Überwachung, überprüfen Sie den aktuellen Status und ändern den aktuellen Status.</span><span class="sxs-lookup"><span data-stu-id="83e09-111">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="83e09-112">Weitere Informationen zum Herunterladen und Installieren der Offline-Status Beispiel-Add-Ins finden Sie unter [Installieren der Offline-Status Beispiel-Add-Ins](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="83e09-112">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="83e09-113">Weitere Informationen zur Status-API finden Sie unter [Über die Offline Zustand-API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="83e09-113">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="83e09-114">Wenn das Add-in offline-Status getrennt ist, müssen Sie implementieren Funktionen zum ordnungsgemäß beendet und bereinigen Sie das Add-in.</span><span class="sxs-lookup"><span data-stu-id="83e09-114">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="83e09-115">Weitere Informationen finden Sie unter [Trennen eines Status Offline-Add-Ins](disconnecting-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="83e09-115">For more information, see [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span></span>
  
## <a name="open-offline-object-routine"></a><span data-ttu-id="83e09-116">Open Offline-Objekt routine</span><span class="sxs-lookup"><span data-stu-id="83e09-116">Open Offline Object routine</span></span>

<span data-ttu-id="83e09-117">Für den Client benachrichtigt werden, wenn Verbindung Status geändert wird müssen Sie die Funktion **[HrOpenOfflineObj](hropenofflineobj.md)** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="83e09-117">For the client to be notified when a connection state change occurs, you must call the **[HrOpenOfflineObj](hropenofflineobj.md)** function.</span></span> <span data-ttu-id="83e09-118">Diese Funktion öffnet ein offline-Objekt, das **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83e09-118">This function opens an offline object that supports **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> <span data-ttu-id="83e09-119">Die **HrOpenOfflineObj** -Funktion ist in der Headerdatei ConnectionState.h definiert.</span><span class="sxs-lookup"><span data-stu-id="83e09-119">The **HrOpenOfflineObj** function is defined in the ConnectionState.h header file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="83e09-120">Die **HrOpenOfflineObj** -Funktion wird in der Headerdatei ImportProcs.h wie folgt deklariert: `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span><span class="sxs-lookup"><span data-stu-id="83e09-120">The **HrOpenOfflineObj** function is declared in the ImportProcs.h header file as follows:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span></span> 
  
### <a name="hropenofflineobj-example"></a><span data-ttu-id="83e09-121">HrOpenOfflineObj-Beispiel</span><span class="sxs-lookup"><span data-stu-id="83e09-121">HrOpenOfflineObj example</span></span>

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a><span data-ttu-id="83e09-122">Initialisieren der Monitor routine</span><span class="sxs-lookup"><span data-stu-id="83e09-122">Initialize Monitor routine</span></span>

<span data-ttu-id="83e09-123">Die `InitMonitor` Funktion ruft die **HrOpenOfflineObj** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="83e09-123">The  `InitMonitor` function calls the **HrOpenOfflineObj** function.</span></span> <span data-ttu-id="83e09-124">Die `InitMonitor` Funktion **CMyOfflineNotify** aufruft, damit Outlook Rückruf Benachrichtigungen an den Client senden kann, und den Rückruf über die Variable **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** registriert `AdviseInfo`.</span><span class="sxs-lookup"><span data-stu-id="83e09-124">The  `InitMonitor` function calls **CMyOfflineNotify** so that Outlook can send callback notifications to the client, and registers the callback through the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** variable  `AdviseInfo`.</span></span>
  
### <a name="initmonitor-example"></a><span data-ttu-id="83e09-125">InitMonitor()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="83e09-125">InitMonitor() example</span></span>

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

## <a name="get-current-state-routine"></a><span data-ttu-id="83e09-126">Abrufen aktueller Zustand routine</span><span class="sxs-lookup"><span data-stu-id="83e09-126">Get Current State routine</span></span>

<span data-ttu-id="83e09-127">Die `GetCurrentState` Funktion ruft die **HrOpenOfflineObj** -Funktion, und klicken Sie dann das offline-Objekt verwendet, um den aktuellen Verbindungsstatus abzurufen.</span><span class="sxs-lookup"><span data-stu-id="83e09-127">The  `GetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to get the current connection state.</span></span> <span data-ttu-id="83e09-128">Der aktuelle Status wird zurückgegeben, der `ulCurState` Variable, die in verwendet wird die `CButtonEventHandler::Click` Funktion, um den aktuellen Status für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83e09-128">The current state is returned in the  `ulCurState` variable, which is used in the  `CButtonEventHandler::Click` function to display the current state to the user.</span></span> 
  
### <a name="getcurrentstate-example"></a><span data-ttu-id="83e09-129">GetCurrentState()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="83e09-129">GetCurrentState() example</span></span>

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

## <a name="set-current-state-routine"></a><span data-ttu-id="83e09-130">Set Aktueller Zustand routine</span><span class="sxs-lookup"><span data-stu-id="83e09-130">Set Current State routine</span></span>

<span data-ttu-id="83e09-131">Die `SetCurrentState` Funktion ruft die **HrOpenOfflineObj** -Funktion, und klicken Sie dann das offline-Objekt verwendet, um den aktuellen Verbindungsstatus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="83e09-131">The  `SetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to set the current connection state.</span></span> <span data-ttu-id="83e09-132">Die `CButtonEventHandler::Click` Funktionsaufrufe der `SetCurrentState` -Funktion und den neuen Zustand übergeben wird über die `ulState` Variable.</span><span class="sxs-lookup"><span data-stu-id="83e09-132">The  `CButtonEventHandler::Click` function calls the  `SetCurrentState` function and the new state is passed in through the  `ulState` variable.</span></span> 
  
### <a name="setcurrentstate-example"></a><span data-ttu-id="83e09-133">SetCurrentState()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="83e09-133">SetCurrentState() example</span></span>

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

## <a name="notification-routine"></a><span data-ttu-id="83e09-134">Benachrichtigungsroutine</span><span class="sxs-lookup"><span data-stu-id="83e09-134">Notification routine</span></span>

<span data-ttu-id="83e09-135">Die Funktion **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** wird von Outlook zum Senden von Benachrichtigungen bei Änderungen in den Verbindungsstatus an einen Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="83e09-135">The **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** function is used by Outlook to send notifications to a client when there are changes in the connection state.</span></span> 
  
### <a name="cmyofflinenotifynotify-example"></a><span data-ttu-id="83e09-136">CMyOfflineNotify::Notify()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="83e09-136">CMyOfflineNotify::Notify() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="83e09-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83e09-137">See also</span></span>

- [<span data-ttu-id="83e09-138">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="83e09-138">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="83e09-139">Installieren des Offlinestatus-Add-In-Beispiels</span><span class="sxs-lookup"><span data-stu-id="83e09-139">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="83e09-140">Informationen zum Offlinestatus-Add-In-Beispiel</span><span class="sxs-lookup"><span data-stu-id="83e09-140">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="83e09-141">Einrichten eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="83e09-141">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="83e09-142">Trennen eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="83e09-142">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

