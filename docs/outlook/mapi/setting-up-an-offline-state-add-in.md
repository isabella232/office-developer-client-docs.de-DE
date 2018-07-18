---
title: Einrichten von einem Add-in auf offline-Status
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a326e93-fe8c-e3a5-1e92-30b75b6cb1d2
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 7b3d0eed6039552813798d4ceb30158444902b36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795522"
---
# <a name="setting-up-an-offline-state-add-in"></a><span data-ttu-id="a3a5d-103">Einrichten von einem Add-in auf offline-Status</span><span class="sxs-lookup"><span data-stu-id="a3a5d-103">Setting up an offline state add-in</span></span>

<span data-ttu-id="a3a5d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3a5d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3a5d-105">Um ein Add-in-offline-Status zu implementieren, müssen Sie die Verbindung, Initialisierung und andere Setup-Funktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-105">To implement an offline state add-in, you must implement connection, initialization, and other setup functions.</span></span> <span data-ttu-id="a3a5d-106">In diesem Thema, diese Verbindung, Initialisierung und Setup werden Funktionen mithilfe von Offline-Status Beispiel-Add-in Codebeispielen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-106">In this topic, these connection, initialization, and setup functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="a3a5d-107">Das Beispiel Offline Zustand-Add-in ist ein COM-add-in, Outlook eine **Offline-Status** -Menü hinzugefügt und State-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-107">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="a3a5d-108">Über das Menü **Offline-Status** können Sie aktivieren oder Deaktivieren der Status der Überwachung, überprüfen Sie den aktuellen Status und ändern den aktuellen Status.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-108">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="a3a5d-109">Weitere Informationen zum Herunterladen und Installieren der Offline-Status Beispiel-Add-Ins finden Sie unter [Installieren der Offline-Status Beispiel-Add-Ins](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="a3a5d-109">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="a3a5d-110">Weitere Informationen zur Status-API finden Sie unter [Über die Offline Zustand-API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="a3a5d-110">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="a3a5d-111">Nachdem Sie ein Add-in-offline-Status eingerichtet, müssen Sie implementieren Funktionen zum Überwachen und Ändern von Änderungen am Status der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-111">After you set up an offline state add-in, you must implement functions to monitor and modify connection state changes.</span></span> <span data-ttu-id="a3a5d-112">Weitere Informationen finden Sie unter [Monitoring Verbindung Zustand Änderungen verwenden ein Add-in Status als offline anzeigen](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="a3a5d-112">For more information, see [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
## <a name="on-connection-routine"></a><span data-ttu-id="a3a5d-113">Klicken Sie auf Verbindung routine</span><span class="sxs-lookup"><span data-stu-id="a3a5d-113">On Connection routine</span></span>

<span data-ttu-id="a3a5d-114">Jedes Mal, wenn ein Add-In geladen wird, wird die **[IDTExtensibility2.OnConnection-Methode](http://msdn.microsoft.com/en-us/library/extensibility.idtextensibility2.onconnection%28v=VS.80%29.aspx)** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-114">The **[IDTExtensibility2.OnConnection Method](http://msdn.microsoft.com/en-us/library/extensibility.idtextensibility2.onconnection%28v=VS.80%29.aspx)** is called every time an add-in is loaded.</span></span> <span data-ttu-id="a3a5d-115">Es ist der Einstiegspunkt für das Add-in, und den Code in eingefügt die `OnConnection` Funktion wird aufgerufen, wenn das Add-In gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-115">It is the entry point for the add-in, so the code you put in the  `OnConnection` function will be called when the add-in starts.</span></span> <span data-ttu-id="a3a5d-116">Im folgenden Beispiel die `OnConnection` Funktionsaufrufe der `HrInitAddin` Funktion.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-116">In the following example, the  `OnConnection` function calls the  `HrInitAddin` function.</span></span> 
  
### <a name="cmyaddinonconnection-example"></a><span data-ttu-id="a3a5d-117">CMyAddin::OnConnection()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3a5d-117">CMyAddin::OnConnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnConnection( 
    IDispatch * Application,  
    ext_ConnectMode ConnectMode,  
    IDispatch * /*AddInInst*/,  
    SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnConnection\n"); 
    HRESULT hRes = S_OK; 
    m_spApp = Application; 
    m_ConnectMode = ConnectMode; 
    if (ConnectMode == ext_cm_AfterStartup) 
        hRes = HrInitAddin(); 
    return hRes; 
}
```

## <a name="initialize-add-in-routine"></a><span data-ttu-id="a3a5d-118">Add-in-Routine initialisieren</span><span class="sxs-lookup"><span data-stu-id="a3a5d-118">Initialize Add-in routine</span></span>

<span data-ttu-id="a3a5d-119">Die `HrInitAddin` Funktionsaufrufe der `LoadLibraries`, `HrCacheProfileName`, und `HrAddMenuItems` Funktionen für das Einrichten des offline-Status-add-ins abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-119">The  `HrInitAddin` function calls the  `LoadLibraries`,  `HrCacheProfileName`, and  `HrAddMenuItems` functions to finish setting up the offline state add-in.</span></span> 
  
### <a name="cmyaddinhrinitaddin-example"></a><span data-ttu-id="a3a5d-120">CMyAddin::HrInitAddin()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3a5d-120">CMyAddin::HrInitAddin() example</span></span>

```cpp
HRESULT CMyAddin::HrInitAddin() 
{ 
    HRESULT hRes = S_OK; 
    LoadLibraries(); 
    hRes = HrCacheProfileName(); 
    Log(true,_T("HrCacheProfileName returned 0x%08X\n"),hRes); 
    hRes = HrAddMenuItems(); 
    Log(true,_T("HrAddMenuItems returned 0x%08X\n"),hRes); 
    return hRes; 
}
```

## <a name="load-libraries-routine"></a><span data-ttu-id="a3a5d-121">Laden Sie Bibliotheken routine</span><span class="sxs-lookup"><span data-stu-id="a3a5d-121">Load Libraries routine</span></span>

<span data-ttu-id="a3a5d-122">Die `LoadLibraries` Funktion lädt die Dynamic Link Library (DLL)-Dateien, die das Add-in benötigt.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-122">The  `LoadLibraries` function loads the dynamic-link library (DLL) files that the add-in requires.</span></span> 
  
### <a name="loadlibraries-example"></a><span data-ttu-id="a3a5d-123">LoadLibraries()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3a5d-123">LoadLibraries() example</span></span>

```cpp
void LoadLibraries() 
{ 
    Log(true,_T("LoadLibraries - loading exports from DLLs\n"));     
    HRESULT hRes = S_OK; 
    UINT uiRet = 0; 
    LONG lRet = 0; 
    BOOL bRet = true; 
    CHAR szSystemDir[MAX_PATH+1] = {0}; 
 
    // Get the system directory path 
    // (mapistub.dll and mapi32.dll reside here) 
    uiRet = GetSystemDirectoryA(szSystemDir, MAX_PATH); 
    if (uiRet > 0) 
    { 
        CHAR szDLLPath[MAX_PATH+1] = {0}; 
        hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, "%s\\%s",  
            szSystemDir, "mapistub.dll"); 
        if (SUCCEEDED(hRes)) 
        { 
            LPFGETCOMPONENTPATH pfnFGetComponentPath = NULL; 
            // Load mapistub.dll 
            hModMAPIStub = LoadLibraryA(szDLLPath); 
            if (hModMAPIStub) 
            {    
                // Get the address of FGetComponentPath from the mapistub 
                pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                    hModMAPIStub, "FGetComponentPath"); 
            } 
            // If there is no address for FGetComponentPath yet 
            // try getting it from mapi32.dll 
            if (!pfnFGetComponentPath) 
            { 
                hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, "%s\\%s", 
                    szSystemDir, "mapi32.dll"); 
                if (SUCCEEDED(hRes)) 
                { 
                    // Load mapi32.dll 
                    hModMAPI = LoadLibraryA(szDLLPath); 
                    if (hModMAPI) 
                    { 
                        // Get the address of FGetComponentPath from mapi32 
                        pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                            hModMAPI, "FGetComponentPath"); 
                    } 
                } 
            } 
            if (pfnFGetComponentPath) 
            { 
                LPSTR szAppLCID = NULL; 
                LPSTR szOfficeLCID = NULL; 
                HKEY hMicrosoftOutlook = NULL; 
                lRet = RegOpenKeyEx( 
                    HKEY_LOCAL_MACHINE, 
                    _T("Software\\Clients\\Mail\\Microsoft Outlook"), 
                    NULL, 
                    KEY_READ, 
                    &hMicrosoftOutlook); 
                if (ERROR_SUCCESS == lRet && hMicrosoftOutlook) 
                { 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, "MSIApplicationLCID", (LPVOID*) &szAppLCID); 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, "MSIOfficeLCID", (LPVOID*) &szOfficeLCID); 
                } 
                if (szAppLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                        "{FF1D0740-D227-11D1-A4B0-006008AF820E}", szAppLCID, szDLLPath, MAX_PATH, true); 
                } 
                if ((!bRet || szDLLPath[0] == _T('\0')) && szOfficeLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                        "{FF1D0740-D227-11D1-A4B0-006008AF820E}", szOfficeLCID, szDLLPath, MAX_PATH, true); 
                } 
                if (!bRet || szDLLPath[0] == _T('\0')) 
                { 
                    bRet = pfnFGetComponentPath( 
                        "{FF1D0740-D227-11D1-A4B0-006008AF820E}", NULL, szDLLPath, MAX_PATH, true); 
                } 
                delete[] szOfficeLCID; 
                delete[] szAppLCID; 
                if (hMicrosoftOutlook) RegCloseKey(hMicrosoftOutlook);       
            } 
            hModMSMAPI = LoadLibrary(szDLLPath); 
            if (hModMSMAPI) 
            { 
                pfnHrOpenOfflineObj = (HROPENOFFLINEOBJ*) GetProcAddress( 
                    hModMSMAPI, 
                    "HrOpenOfflineObj@20"); 
                pfnMAPIFreeBuffer = (LPMAPIFREEBUFFER) GetProcAddress( 
                    hModMSMAPI, 
                    "MAPIFreeBuffer"); 
            } 
        } 
    }    
}
```

## <a name="cache-profile-name-routine"></a><span data-ttu-id="a3a5d-124">Name der Benutzerprofildienst-Routine Cache</span><span class="sxs-lookup"><span data-stu-id="a3a5d-124">Cache Profile Name routine</span></span>

<span data-ttu-id="a3a5d-125">Die `HrCacheProfileName` Funktion ruft die **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** -Funktion, um einen Profilabschnitt für die aktuelle Sitzung zu öffnen, und klicken Sie dann das Profil für die Schaltflächenhandler festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-125">The  `HrCacheProfileName` function calls the **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function to open a profile section for the current session, and then sets the profile for the button handlers.</span></span> 
  
### <a name="cmyaddinhrcacheprofilename-example"></a><span data-ttu-id="a3a5d-126">CMyAddin::HrCacheProfileName()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3a5d-126">CMyAddin::HrCacheProfileName() example</span></span>

```cpp
HRESULT CMyAddin::HrCacheProfileName() 
{ 
    HRESULT hRes = S_OK;     
    _NameSpacePtr spSession = m_spApp->GetNamespace("MAPI"); 
    IUnknown* lpMAPIObject = NULL; 
    LPMAPISESSION lpMAPISession = NULL; 
    // use the raw accessor 
    hRes = spSession->get_MAPIOBJECT(&lpMAPIObject); 
    if (SUCCEEDED(hRes) && lpMAPIObject) 
    { 
        hRes = lpMAPIObject->QueryInterface(IID_IMAPISession,(LPVOID*)&lpMAPISession); 
    } 
    if (SUCCEEDED(hRes) && lpMAPISession) 
    { 
        LPPROFSECT lpPSGlobal = NULL; 
        hRes = lpMAPISession->OpenProfileSection((LPMAPIUID)pbGlobalProfileSectionGuid, NULL, 0, &lpPSGlobal); 
 
        if (SUCCEEDED(hRes) && lpPSGlobal) 
        { 
            LPSPropValue lpProfileName = NULL; 
            // Asking for PR_PROFILE_NAME_W here - this might not work with earlier versions of Outlook 
            SPropTagArray staga = {1,PR_PROFILE_NAME_W}; 
            ULONG cVal = 0; 
            hRes = lpPSGlobal->GetProps(&staga,0,&cVal,&lpProfileName); 
            if (SUCCEEDED(hRes) && 1 == cVal && lpProfileName && PR_PROFILE_NAME_W == lpProfileName->ulPropTag) 
            { 
                m_InitButtonHandler.SetProfile(lpProfileName->Value.lpszW); 
                m_GetStateButtonHandler.SetProfile(lpProfileName->Value.lpszW); 
                m_SetStateButtonHandler.SetProfile(lpProfileName->Value.lpszW); 
            } 
            if (pfnMAPIFreeBuffer) pfnMAPIFreeBuffer(lpProfileName); 
        } 
        if (lpPSGlobal) lpPSGlobal->Release(); 
    } 
    if (lpMAPISession) lpMAPISession->Release(); 
    return hRes; 
}
```

## <a name="add-menu-items-routine"></a><span data-ttu-id="a3a5d-127">Hinzufügen von Menüelementen routine</span><span class="sxs-lookup"><span data-stu-id="a3a5d-127">Add Menu Items routine</span></span>

<span data-ttu-id="a3a5d-128">Die `HrAddMenuItems` Funktion definiert die Optionen, die unter der **Status als offline anzeigen** im Menü angezeigt, die erstellt wird werden, wenn das Add-in in Outlook geladen wird, und dann ruft `DispEventAdvise` für jedes Menüelement im.</span><span class="sxs-lookup"><span data-stu-id="a3a5d-128">The  `HrAddMenuItems` function defines the menu options that appear under the **Offline State** menu that is created when the add-in is loaded in Outlook, and then calls  `DispEventAdvise` for each menu item.</span></span> 
  
### <a name="cmyaddinhraddmenuitems-example"></a><span data-ttu-id="a3a5d-129">CMyAddin::HrAddMenuItems()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3a5d-129">CMyAddin::HrAddMenuItems() example</span></span>

```cpp
HRESULT CMyAddin::HrAddMenuItems() 
{ 
    Log(true,"HrAddMenuItems\n"); 
    HRESULT    hRes = S_OK; 
    if (!m_fMenuItemsAdded) 
    { 
        try 
        { 
            _ExplorerPtr spExplorer = m_spApp->ActiveExplorer(); 
            _CommandBarsPtr spCmdBars = spExplorer->__CommandBars; 
            CommandBarPtr spMainBar = spCmdBars->ActiveMenuBar; 
            CommandBarControlsPtr spMainCtrls = spMainBar->Controls; 
 
            try { m_spMyMenu = spMainCtrls->GetItem("Offline State"); } catch (_com_error) {} 
            if (m_spMyMenu == NULL) 
            {             
                m_spMyMenu = spMainCtrls->Add((long)msoControlPopup,vtMissing,vtMissing,vtMissing, true); 
                m_spMyMenu->Caption = "Offline State"; 
            } 
 
            CommandBarControlsPtr spMyMenuCtrls = m_spMyMenu->Controls; 
            try { m_spInitButton = spMyMenuCtrls->GetItem("&Init Monitor"); } catch (_com_error) {} 
            if (m_spInitButton == NULL) 
            { 
                m_spInitButton = spMyMenuCtrls->Add((long)msoControlButton, vtMissing, vtMissing, vtMissing, true); 
                m_spInitButton->Caption = "&Init Monitor"; 
                m_spInitButton->FaceId = MY_INIT_BUTTON; 
            } 
            try { m_spDeinitButton = spMyMenuCtrls->GetItem("&Deinit Monitor"); } catch (_com_error) {} 
            if (m_spDeinitButton == NULL) 
            { 
                m_spDeinitButton = spMyMenuCtrls->Add((long)msoControlButton, vtMissing, vtMissing, vtMissing, true); 
                m_spDeinitButton->Caption = "&Deinit Monitor"; 
                m_spDeinitButton->FaceId = MY_DEINIT_BUTTON; 
            } 
            try { m_spGetStateButton = spMyMenuCtrls->GetItem("&GetCurrentState"); } catch (_com_error) {} 
            if (m_spGetStateButton == NULL) 
            { 
                m_spGetStateButton = spMyMenuCtrls->Add((long)msoControlButton, vtMissing, vtMissing, vtMissing, true); 
                m_spGetStateButton->Caption = "&GetCurrentState"; 
                m_spGetStateButton->FaceId = MY_GETSTATE_BUTTON; 
            } 
            try { m_spSetStateButton = spMyMenuCtrls->GetItem("&SetCurrentState"); } catch (_com_error) {} 
            if (m_spSetStateButton == NULL) 
            { 
                m_spSetStateButton = spMyMenuCtrls->Add((long)msoControlButton, vtMissing, vtMissing, vtMissing, true); 
                m_spSetStateButton->Caption = "&SetCurrentState"; 
                m_spSetStateButton->FaceId = MY_SETSTATE_BUTTON; 
            } 
            // Set up advise 
            _com_util::CheckError(m_InitButtonHandler.DispEventAdvise(m_spInitButton)); 
            _com_util::CheckError(m_DeinitButtonHandler.DispEventAdvise(m_spDeinitButton)); 
            _com_util::CheckError(m_GetStateButtonHandler.DispEventAdvise(m_spGetStateButton)); 
            _com_util::CheckError(m_SetStateButtonHandler.DispEventAdvise(m_spSetStateButton)); 
        } 
        catch (_com_error) 
        { 
            hRes = E_FAIL; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            m_fMenuItemsAdded = true; 
        } 
    } 
    return hRes;  
}
```

## <a name="see-also"></a><span data-ttu-id="a3a5d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3a5d-130">See also</span></span>

- [<span data-ttu-id="a3a5d-131">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="a3a5d-131">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="a3a5d-132">Installieren des Offlinestatus-Add-In-Beispiels</span><span class="sxs-lookup"><span data-stu-id="a3a5d-132">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="a3a5d-133">Informationen zum Offlinestatus-Add-In-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3a5d-133">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="a3a5d-134">Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In</span><span class="sxs-lookup"><span data-stu-id="a3a5d-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
- [<span data-ttu-id="a3a5d-135">Trennen eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="a3a5d-135">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

