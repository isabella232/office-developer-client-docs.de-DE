---
title: Anmelden bei einem Anbieter von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Zuletzt geändert: 02 Juli, 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307819"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Anmelden bei einem Anbieter von umschlossenem PST-Speicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie MAPI bei einem eingebundenen PST-Speicheranbieter anmelden können, müssen Sie den eingebundenen PST-Speicheranbieter initialisieren und konfigurieren. Weitere Informationen finden Sie unter [Initialisieren eines EingebundenEN PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md).
  
Nachdem Sie einen eingebundenen PST-Speicheranbieter initialisiert und konfiguriert haben, müssen Sie zwei Anmelde Routinen implementieren. Die **[IMSProvider:: LOGON](imsprovider-logon.md)** -Funktion meldet MAPI für den eingebundenen PST-Speicheranbieter an. Die **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** -Funktion meldet den MAPI-Spooler für den eingebundenen PST-Speicheranbieter an. 
  
In diesem Thema werden die **IMSProvider:: LOGON** -Funktion und die **IMSProvider:: SpoolerLogon** -Funktion mithilfe von Codebeispielen aus dem beispielsWEISE einGebundenen PST-Speicheranbieter demonstriert. Im Beispiel wird ein eingebundener PST-Anbieter implementiert, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum herunterladen und Installieren des eingeWickelten Beispiel-PST-Speicheranbieters finden Sie unter [Installing the Sample Wrapped Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikations-API finden Sie unter Informationen zur [Replikations-API](about-the-replication-api.md).
  
Nachdem MAPI und der MAPI-Spooler beim eingebundenen PST-Speicheranbieter angemeldet sind, können Sie diese verwenden. Weitere Informationen finden Sie unter [Verwenden eines EingebundenEN PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>MAPI-Anmelderoutine

Nachdem der eingebundene PST-Speicheranbieter initialisiert wurde, müssen Sie die **[IMSProvider:: LOGON](imsprovider-logon.md)** -Funktion implementieren, um sich bei MAPI im eingebundenen PST-Speicher anzumelden. Diese Funktion überprüft Benutzeranmeldeinformationen und ruft die Konfigurationseigenschaften für den Anbieter ab. Sie müssen auch die `SetOLFIInOST` Funktion zum Festlegen der Offline Datei Info (**[OLFI](olfi.md)** ) implementieren. **OLFI** ist eine Warteschlange von langfristigen ID-Strukturen, die vom eingebundenen PST-Speicheranbieter zum Zuweisen einer EINTRAGS-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus verwendet wird. Schließlich gibt die **IMSProvider:: LOGON** -Funktion ein Nachrichtenspeicherobjekt zurück, das von der MAPI-Spooler-und der Client `ppMDB` Anwendung im Parameter angemeldet werden kann. 
  
### <a name="cmsproviderlogon-example"></a>CMSProvider:: LOGON () (Beispiel)

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a>MAPI-Spooler-Anmelderoutine

Ähnlich wie **IMSProvider:: LOGON**müssen Sie die **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** -Funktion implementieren, um den MAPI-Spooler für den eingebundenen PST-Speicher zu protokollieren. Ein Nachrichtenspeicherobjekt, an das sich die MAPI-Warteschlange und die Clientanwendungen anmelden können, `ppMDB` wird im-Parameter zurückgegeben. 
  
### <a name="cmsproviderspoolerlogon-example"></a>CMSProvider:: SpoolerLogon ()-Beispiel

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a>Siehe auch

- [Informationen zum einGebundenen PST-Speicheranbieter](about-the-sample-wrapped-pst-store-provider.md) 
- [Installieren des eingeWickelten Beispiel-PST-Speicheranbieters](installing-the-sample-wrapped-pst-store-provider.md) 
- [Initialisieren eines einGebundenen PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md)
- [Verwenden eines einGebundenen PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines einGebundenen PST-Speicheranbieters](shutting-down-a-wrapped-pst-store-provider.md)

