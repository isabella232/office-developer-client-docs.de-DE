---
title: Anmelden bei einem gepackten PST-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Zuletzt geändert: 02 Juli 2012'
ms.openlocfilehash: 0716017788239c22f31007438089118d109010a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570478"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Anmelden bei einem gepackten PST-Anbieter

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bevor Sie zu einem gepackten PST-Speicher-Anbieter auf MAPI anmelden können, müssen Sie initialisieren und konfigurieren den gepackten Anbieter für Persönliche Ordner-Datei (PST) anmelden. Weitere Informationen finden Sie unter [einem umfließendem PST-Anbieter zu initialisieren](initializing-a-wrapped-pst-store-provider.md).
  
Nachdem Sie initialisiert und einen gepackten PST-Anbieter konfiguriert haben, müssen Sie zwei Anmeldung Routinen implementieren. Die Funktion **[IMSProvider::Logon](imsprovider-logon.md)** anmeldet MAPI auf die gepackten PST-Anbieter. Die Funktion **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** meldet sich die MAPI-Warteschlange auf dem gepackten PST-Anbieter. 
  
In diesem Thema werden die **IMSProvider::Logon** und der **IMSProvider::SpoolerLogon** -Funktion mithilfe von Codebeispielen aus der umbrochen PST Store Beispielanbieter veranschaulicht. Das Beispiel implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter finden Sie unter [Sample umfließendem PST Store Provider installieren](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).
  
Nachdem MAPI- und die MAPI-Warteschlange angemeldet sind bei der gepackten PST-Speicheranbieter ist, verwendet werden. Weitere Informationen finden Sie unter [Verwenden von einem umfließendem PST-Anbieter](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>MAPI-Anmeldung routine

Nachdem der gepackten PST-Speicheranbieter initialisiert wurde, müssen Sie die **[IMSProvider::Logon](imsprovider-logon.md)** -Funktion zum Anmelden MAPI an den gepackten PST Store implementieren. Diese Funktion überprüft die Anmeldeinformationen und ruft die Konfigurationseigenschaften für den Anbieter. Sie müssen auch Implementieren der `SetOLFIInOST` -Funktion zum Festlegen der Offline Dateiinformationen (**[OLFI](olfi.md)** ). **OLFI** ist eine Warteschlange der langfristigen ID Strukturen, die von der gepackten PST-Anbieter verwendet wird, weisen Sie eine Eintrags-ID für eine neue Nachricht oder einen Ordner im Offlinemodus. Schließlich gibt die Funktion **IMSProvider::Logon** ein Nachricht Store-Objekt, das die MAPI-Warteschlange und Clientanwendungen in anmelden können der `ppMDB` Parameter. 
  
### <a name="cmsproviderlogon-example"></a>CMSProvider::Logon()-Beispiel

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

## <a name="mapi-spooler-logon-routine"></a>MAPI-Warteschlange Anmeldung routine

Ähnlich wie **IMSProvider::Logon**, müssen Sie die **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** -Funktion, um die MAPI-Warteschlange an den gepackten PST-Speicher melden implementieren. Eine Nachricht Store-Objekt, das die MAPI-Warteschlange und Clientanwendungen anmelden können returned in der `ppMDB` Parameter. 
  
### <a name="cmsproviderspoolerlogon-example"></a>CMSProvider::SpoolerLogon()-Beispiel

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

- [Informationen über das Beispiel für einen Anbieter von umschlossenem PST-Speicher](about-the-sample-wrapped-pst-store-provider.md) 
- [Installieren des Beispiel für einen Anbieter von umschlossenem PST-Speicher](installing-the-sample-wrapped-pst-store-provider.md) 
- [Initialisieren eines Anbieters von umschlossenem PST-Speicher](initializing-a-wrapped-pst-store-provider.md)
- [Verwenden eines Anbieters von umschlossenem PST-Speicher](using-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines Anbieters von umschlossenem PST-Speicher](shutting-down-a-wrapped-pst-store-provider.md)

