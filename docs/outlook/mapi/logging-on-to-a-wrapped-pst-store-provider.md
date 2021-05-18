---
title: Anmelden bei einem Anbieter von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Letzte Änderung: 02. Juli 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408986"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Anmelden bei einem Anbieter von umschlossenem PST-Speicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie sich bei mapI bei einem umschlossenen ANBIETER für den PST-Speicher anmelden können, müssen Sie den umschlossenen Anbieter für persönliche Ordner (PST) initialisieren und konfigurieren. Weitere Informationen finden Sie unter [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).
  
Nachdem Sie einen umschlossenen PST Store-Anbieter initialisiert und konfiguriert haben, müssen Sie zwei Anmelderoutinen implementieren. Die **[IMSProvider::Logon-Funktion](imsprovider-logon.md)** meldet sich auf MAPI an den umschlossenen ANBIETER des PST-Speichers. Die **[IMSProvider::SpoolerLogon-Funktion](imsprovider-spoolerlogon.md)** protokolliert im MAPI-Spooler an den umschlossenen PST-Speicheranbieter. 
  
In diesem Thema werden die **IMSProvider::Logon-Funktion** und die **IMSProvider::SpoolerLogon-Funktion** anhand von Codebeispielen aus dem Beispiel umschlossenen PST Store demonstriert. Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren des Beispielanbieters für umbrochene PST Store finden Sie unter [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikations-API finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).
  
Nachdem MAPI und der MAPI-Spooler beim umschlossenen ANBIETER für den PST Store angemeldet sind, kann er verwendet werden. Weitere Informationen finden Sie unter [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>MAPI-Anmelderoutine

Nachdem der umschlossene ANBIETER für den PST-Speicher initialisiert wurde, müssen Sie die **[IMSProvider::Logon-Funktion](imsprovider-logon.md)** implementieren, um mapI beim umschlossenen PST-Speicher zu protokollieren. Diese Funktion überprüft Benutzeranmeldeinformationen und ruft die Konfigurationseigenschaften für den Anbieter ab. Sie müssen auch die Funktion `SetOLFIInOST` implementieren, um die Offlinedateiinformationen ( OLFI )**[festlegen zu können.](olfi.md)** **OLFI** ist eine Warteschlange mit langfristigen ID-Strukturen, die vom umschlossenen Pst Store-Anbieter zum Zuweisen einer Eintrags-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus verwendet wird. Schließlich gibt die **IMSProvider::Logon-Funktion** ein Nachrichtenspeicherobjekt zurück, an das sich der MAPI-Spooler und die Clientanwendungen im Parameter anmelden  `ppMDB` können. 
  
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

## <a name="mapi-spooler-logon-routine"></a>MAPI-Spooler-Anmelderoutine

Ähnlich wie **IMSProvider::Logon** müssen Sie die **[IMSProvider::SpoolerLogon-Funktion](imsprovider-spoolerlogon.md)** implementieren, um den MAPI-Spooler im umschlossenen PST-Speicher zu protokollieren. Ein Nachrichtenspeicherobjekt, an dem sich der MAPI-Spooler und die Clientanwendungen anmelden können, wird im Parameter  `ppMDB` zurückgegeben. 
  
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

- [Informationen zum Beispiel umschlossenen STORE Anbieter](about-the-sample-wrapped-pst-store-provider.md) 
- [Installieren des Umschlossenen Store -Beispielanbieters](installing-the-sample-wrapped-pst-store-provider.md) 
- [Initialisieren eines umschlossenen STORE Anbieters](initializing-a-wrapped-pst-store-provider.md)
- [Verwenden eines umschlossenen STORE Anbieters](using-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines umschlossenen STORE Anbieters](shutting-down-a-wrapped-pst-store-provider.md)

