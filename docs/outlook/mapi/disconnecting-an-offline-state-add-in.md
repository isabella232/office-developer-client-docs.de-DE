---
title: Trennen eines Offlinestatus-Add-Ins
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Zuletzt geändert: 07. Dezember 2015'
ms.openlocfilehash: c665bae57a72428df7acd92e080f7c31b131253b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316653"
---
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="912ad-103">Trennen eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="912ad-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="912ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="912ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="912ad-105">Wenn das Offlinestatus-Add-In getrennt wird, müssen Sie Funktionen implementieren, um das Add-In ordnungsgemäß zu beenden und zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="912ad-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="912ad-106">Weitere Informationen zum Einrichten und Verwenden des Offlinestatus-Add-Ins finden Sie unter [Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md) und [Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="912ad-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="912ad-107">In diesem Thema werden diese Funktionen zum Trennen, Beenden und Bereinigen anhand von Codebeispielen aus dem Offlinestatus-Add-In-Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="912ad-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="912ad-108">Das Offlinestatus-Add-In-Beispiel ist ein COM-Add-In, das ein **Offlinestatus**-Menü zu Outlook hinzufügt und die Offlinestatus-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="912ad-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="912ad-109">Über das Menü „Offlinestatus“ können Sie die Statusüberwachung aktivieren oder deaktivieren, den aktuellen Status überprüfen und den aktuellen Status ändern.</span><span class="sxs-lookup"><span data-stu-id="912ad-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="912ad-110">Weitere Informationen zum Herunterladen und Installieren des Offlinestatus-Add-In-Beispiels finden Sie unter [Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="912ad-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="912ad-111">Weitere Informationen zur Offlinestatus-API finden Sie unter [Informationen zur Offlinestatus-API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="912ad-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="912ad-112">Informationen zur Trennungsroutine</span><span class="sxs-lookup"><span data-stu-id="912ad-112">On Disconnection Routine</span></span>

<span data-ttu-id="912ad-113">Die **IDTExtensibility2.OnDisconnection**-Methode wird aufgerufen, wenn das Offlinestatus-Add-In entladen wird.</span><span class="sxs-lookup"><span data-stu-id="912ad-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="912ad-114">In diese Funktion sollte ein Bereinigungscode implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="912ad-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="912ad-115">Im folgenden Beispiel ruft die **IDTExtensibility2.OnDisconnection**-Funktion die `HrTermAddin`-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="912ad-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="912ad-116">Beispiel für CMyAddin::OnDisconnection()</span><span class="sxs-lookup"><span data-stu-id="912ad-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="912ad-117">Add-In-Funktion zum Beenden</span><span class="sxs-lookup"><span data-stu-id="912ad-117">Terminate Add-in Function</span></span>

<span data-ttu-id="912ad-118">Die `HrTermAddin`-Funktion ruft die Funktionen `inDeInitMonitor`, `HrRemoveMenuItems` und `UnloadLibraries` auf, um das Bereinigen des Offlinestatus-Add-Ins zu beenden.</span><span class="sxs-lookup"><span data-stu-id="912ad-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="912ad-119">Beispiel für CMyAddin::HrTermAddin()</span><span class="sxs-lookup"><span data-stu-id="912ad-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="912ad-120">Routine zum Aufheben der Initialisierung der Überwachung</span><span class="sxs-lookup"><span data-stu-id="912ad-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="912ad-121">Die `inDeInitMonitor`-Funktion ruft die [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)-Funktion auf, um die Rückrufe für das Offlineprojekt abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="912ad-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="912ad-122">Beispiel für DeInitMonitor()</span><span class="sxs-lookup"><span data-stu-id="912ad-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="912ad-123">Routine zum Entfernen von Menüelementen</span><span class="sxs-lookup"><span data-stu-id="912ad-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="912ad-124">Die `HrRemoveMenuItems`-Funktion ruft `DispEventUnadvise` für jedes Menüelement im Menü **Offlinestatus** auf und löscht dann das Menü **Offlinestatus**.</span><span class="sxs-lookup"><span data-stu-id="912ad-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="912ad-125">Beispiel für CMyAddin::HrRemoveMenuItems()</span><span class="sxs-lookup"><span data-stu-id="912ad-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="912ad-126">Routine zum Entladen von Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="912ad-126">Unload Libraries Routine</span></span>

<span data-ttu-id="912ad-127">Wenn das Add-in von Outlook entladen wird, entlädt die `UnloadLibraries`-Funktion entfernt die DLL-Dateien (Dynamic Link Libraries), die für das Add-In erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="912ad-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="912ad-128">Beispiel für UnloadLibraries()</span><span class="sxs-lookup"><span data-stu-id="912ad-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="912ad-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="912ad-129">See also</span></span>

- [<span data-ttu-id="912ad-130">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="912ad-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="912ad-131">Installieren des Offlinestatus-Add-In-Beispiels</span><span class="sxs-lookup"><span data-stu-id="912ad-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="912ad-132">Informationen zum Offlinestatus-Add-In-Beispiel</span><span class="sxs-lookup"><span data-stu-id="912ad-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="912ad-133">Einrichten eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="912ad-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="912ad-134">Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In</span><span class="sxs-lookup"><span data-stu-id="912ad-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

