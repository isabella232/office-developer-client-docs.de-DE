---
title: Trennen eines Offlinestatus-Add-Ins
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Letzte Änderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 82f529f58a62f412ed8b25d1ceaf508463491612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791542"
---
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="76161-103">Trennen eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="76161-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="76161-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76161-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76161-105">Wenn das Add-in offline-Status getrennt ist, müssen Sie implementieren Funktionen zum ordnungsgemäß beendet und bereinigen Sie das Add-in.</span><span class="sxs-lookup"><span data-stu-id="76161-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="76161-106">Weitere Informationen zum Einrichten und im Offlinemodus state-add-in zum Überwachen von Änderungen am Status von Verbindung finden Sie unter [Einstellung von einer Offline-Status-Add-in](setting-up-an-offline-state-add-in.md) und [Monitoring Verbindung Zustand Änderungen mithilfe einer Offline-Status-Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="76161-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="76161-107">In diesem Thema, diese Trennung beenden und Bereinigungscode Funktionen werden mithilfe von Offline-Status Beispiel-Add-in Codebeispielen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="76161-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="76161-108">Das Beispiel Offline Zustand-Add-in ist ein COM-add-in, Outlook eine **Offline-Status** -Menü hinzugefügt und State-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="76161-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="76161-109">Über das Menü Offline-Status können Sie aktivieren oder Deaktivieren der Status der Überwachung, überprüfen Sie den aktuellen Status und ändern den aktuellen Status.</span><span class="sxs-lookup"><span data-stu-id="76161-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="76161-110">Weitere Informationen zum Herunterladen und Installieren der Offline-Status Beispiel-Add-Ins finden Sie unter [Installieren der Offline-Status Beispiel-Add-Ins](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="76161-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="76161-111">Weitere Informationen zur Status-API finden Sie unter [Über die Offline Zustand-API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="76161-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="76161-112">Klicken Sie auf Trennen von Routine</span><span class="sxs-lookup"><span data-stu-id="76161-112">On Disconnection Routine</span></span>

<span data-ttu-id="76161-113">Die **IDTExtensibility2.OnDisconnection** -Methode wird aufgerufen, wenn das Add-in Offline-Status entladen wird.</span><span class="sxs-lookup"><span data-stu-id="76161-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="76161-114">Implementieren Sie Bereinigung von Code in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="76161-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="76161-115">Im folgenden Beispiel wird die Funktion **IDTExtensibility2.OnDisconnection** Ruft die `HrTermAddin` Funktion.</span><span class="sxs-lookup"><span data-stu-id="76161-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="76161-116">CMyAddin::OnDisconnection()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="76161-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="76161-117">Beenden Sie die Add-in-Funktion</span><span class="sxs-lookup"><span data-stu-id="76161-117">Terminate Add-in Function</span></span>

<span data-ttu-id="76161-118">Die `HrTermAddin` Funktionsaufrufe der `inDeInitMonitor`, `HrRemoveMenuItems`, und `UnloadLibraries` Funktionen zum Bereinigen des Status Offline-Add-Ins Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="76161-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="76161-119">CMyAddin::HrTermAddin()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="76161-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="76161-120">Monitor Routine deinitialize</span><span class="sxs-lookup"><span data-stu-id="76161-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="76161-121">Die `inDeInitMonitor` Funktion ruft die [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) -Funktion, um die Rückrufe für das offline-Objekt abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="76161-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="76161-122">DeInitMonitor()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="76161-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="76161-123">Entfernen Sie im Menü Elemente Routine</span><span class="sxs-lookup"><span data-stu-id="76161-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="76161-124">Die `HrRemoveMenuItems` Funktionsaufrufe `DispEventUnadvise` für jedes Menüelement im, zeigen Sie im Menü **Offline-Status** und löscht dann das Menü **Status als offline anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="76161-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="76161-125">CMyAddin::HrRemoveMenuItems()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="76161-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="76161-126">Unload Bibliotheken Routine</span><span class="sxs-lookup"><span data-stu-id="76161-126">Unload Libraries Routine</span></span>

<span data-ttu-id="76161-127">Wenn das Add-In entladen aus Outlook, wird die `UnloadLibraries` Funktion entlädt das Dynamic Link Libraries (DLLs), die für das Add-in erforderlich.</span><span class="sxs-lookup"><span data-stu-id="76161-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="76161-128">UnloadLibraries()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="76161-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="76161-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76161-129">See also</span></span>

- [<span data-ttu-id="76161-130">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="76161-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="76161-131">Installieren des Offlinestatus-Add-In-Beispiels</span><span class="sxs-lookup"><span data-stu-id="76161-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="76161-132">Informationen zum Offlinestatus-Add-In-Beispiel</span><span class="sxs-lookup"><span data-stu-id="76161-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="76161-133">Einrichten eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="76161-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="76161-134">Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In</span><span class="sxs-lookup"><span data-stu-id="76161-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

