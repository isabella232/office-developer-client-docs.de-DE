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
# <a name="disconnecting-an-offline-state-add-in"></a>Trennen eines Offlinestatus-Add-Ins

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn das Offlinestatus-Add-In getrennt wird, müssen Sie Funktionen implementieren, um das Add-In ordnungsgemäß zu beenden und zu bereinigen. Weitere Informationen zum Einrichten und Verwenden des Offlinestatus-Add-Ins finden Sie unter [Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md) und [Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
In diesem Thema werden diese Funktionen zum Trennen, Beenden und Bereinigen anhand von Codebeispielen aus dem Offlinestatus-Add-In-Beispiel veranschaulicht. Das Offlinestatus-Add-In-Beispiel ist ein COM-Add-In, das ein **Offlinestatus**-Menü zu Outlook hinzufügt und die Offlinestatus-API verwendet. Über das Menü „Offlinestatus“ können Sie die Statusüberwachung aktivieren oder deaktivieren, den aktuellen Status überprüfen und den aktuellen Status ändern. Weitere Informationen zum Herunterladen und Installieren des Offlinestatus-Add-In-Beispiels finden Sie unter [Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md). Weitere Informationen zur Offlinestatus-API finden Sie unter [Informationen zur Offlinestatus-API](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>Informationen zur Trennungsroutine

Die **IDTExtensibility2.OnDisconnection**-Methode wird aufgerufen, wenn das Offlinestatus-Add-In entladen wird. In diese Funktion sollte ein Bereinigungscode implementiert werden. Im folgenden Beispiel ruft die **IDTExtensibility2.OnDisconnection**-Funktion die `HrTermAddin`-Funktion auf. 
  
### <a name="cmyaddinondisconnection-example"></a>Beispiel für CMyAddin::OnDisconnection()

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>Add-In-Funktion zum Beenden

Die `HrTermAddin`-Funktion ruft die Funktionen `inDeInitMonitor`, `HrRemoveMenuItems` und `UnloadLibraries` auf, um das Bereinigen des Offlinestatus-Add-Ins zu beenden. 
  
### <a name="cmyaddinhrtermaddin-example"></a>Beispiel für CMyAddin::HrTermAddin()

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

## <a name="deinitialize-monitor-routine"></a>Routine zum Aufheben der Initialisierung der Überwachung

Die `inDeInitMonitor`-Funktion ruft die [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)-Funktion auf, um die Rückrufe für das Offlineprojekt abzubrechen. 
  
### <a name="deinitmonitor-example"></a>Beispiel für DeInitMonitor()

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

## <a name="remove-menu-items-routine"></a>Routine zum Entfernen von Menüelementen

Die `HrRemoveMenuItems`-Funktion ruft `DispEventUnadvise` für jedes Menüelement im Menü **Offlinestatus** auf und löscht dann das Menü **Offlinestatus**. 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>Beispiel für CMyAddin::HrRemoveMenuItems()

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

## <a name="unload-libraries-routine"></a>Routine zum Entladen von Bibliotheken

Wenn das Add-in von Outlook entladen wird, entlädt die `UnloadLibraries`-Funktion entfernt die DLL-Dateien (Dynamic Link Libraries), die für das Add-In erforderlich sind. 
  
### <a name="unloadlibraries-example"></a>Beispiel für UnloadLibraries()

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

- [Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
- [Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md)
- [Informationen zum Offlinestatus-Add-In-Beispiel](about-the-sample-offline-state-add-in.md)
- [Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md)
- [Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

