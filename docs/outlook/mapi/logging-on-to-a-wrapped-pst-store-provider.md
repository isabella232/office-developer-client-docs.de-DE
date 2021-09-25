---
title: Anmelden bei einem Anbieter von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 1015611fea9b8080ba201855b6a1847c84bdc47a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579649"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Anmelden bei einem Anbieter von umschlossenem PST-Speicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie sich bei einem anbieter umschlossenen PST-Speicher anmelden können, müssen Sie den Anbieter des PST-Speichers (Wrapped Personal Folders File) initialisieren und konfigurieren. Weitere Informationen finden Sie unter [Initialisieren eines umschlossenen PST-Store Anbieters.](initializing-a-wrapped-pst-store-provider.md)
  
Nachdem Sie einen anbieter umschlossenen PST-Speicher initialisiert und konfiguriert haben, müssen Sie zwei Anmelderoutinen implementieren. Die **[IMSProvider::Logon-Funktion](imsprovider-logon.md)** meldet sich auf der MAPI beim anbieterumschlossenen PST-Speicher an. Die **[IMSProvider::SpoolerLogon-Funktion](imsprovider-spoolerlogon.md)** meldet sich im MAPI-Spooler beim anbieterumschlossenen PST-Speicher an. 
  
In diesem Thema werden die **IMSProvider::Logon-Funktion** und die **IMSProvider::SpoolerLogon-Funktion** anhand von Codebeispielen aus dem Beispiel für ein umschlossenes PST-Store-Anbieter veranschaulicht. Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren des Beispiel-Anbieters für umbrochene PST-Store finden Sie unter [Installieren des Beispiels für einen umschlossenen PST-Store Anbieter.](installing-the-sample-wrapped-pst-store-provider.md) Weitere Informationen zur Replikations-API finden Sie unter ["Informationen zur Replikations-API".](about-the-replication-api.md)
  
Nachdem DIE MAPI und der MAPI-Spooler beim Anbieter des umschlossenen PST-Speichers angemeldet wurden, kann sie verwendet werden. Weitere Informationen finden Sie unter [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>MAPI-Anmelderoutine

Nachdem der Anbieter des umschlossenen PST-Speichers initialisiert wurde, müssen Sie die **[IMSProvider::Logon-Funktion](imsprovider-logon.md)** implementieren, um die MAPI am umschlossenen PST-Speicher anzumelden. Diese Funktion überprüft benutzeranmeldeinformationen und ruft die Konfigurationseigenschaften für den Anbieter ab. Sie müssen auch die  `SetOLFIInOST` Funktion implementieren, um die Offlinedateiinformationen **[(OLFI)](olfi.md)** festzulegen. **OLFI** ist eine Warteschlange mit langfristigen ID-Strukturen, die vom Anbieter des umschlossenen PST-Speichers verwendet wird, um eine Eintrags-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus zuzuweisen. Schließlich gibt die **IMSProvider::Logon-Funktion** ein Nachrichtenspeicherobjekt zurück, bei dem sich mapi-Spooler und Clientanwendungen im Parameter anmelden  `ppMDB` können. 
  
### <a name="cmsproviderlogon-example"></a>CMSProvider::Logon() (Beispiel)

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

Ähnlich wie **IMSProvider::Logon** müssen Sie die **[IMSProvider::SpoolerLogon-Funktion](imsprovider-spoolerlogon.md)** implementieren, um den MAPI-Spooler im umschlossenen PST-Speicher zu protokollieren. Ein Nachrichtenspeicherobjekt, bei dem sich mapi-Spooler und Clientanwendungen anmelden können, wird im  `ppMDB` Parameter zurückgegeben. 
  
### <a name="cmsproviderspoolerlogon-example"></a>CMSProvider::SpoolerLogon() (Beispiel)

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

- [Informationen zum Beispiel für pst-Store-Anbieter mit Umschlossenen](about-the-sample-wrapped-pst-store-provider.md) 
- [Installieren des PsT-Beispielanbieters Store](installing-the-sample-wrapped-pst-store-provider.md) 
- [Initialisieren eines Anbieters von umschlossenen PST-Store](initializing-a-wrapped-pst-store-provider.md)
- [Verwenden eines Anbieters von umschlossenen PST-Store](using-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines Anbieters von umschlossenen PST-Store](shutting-down-a-wrapped-pst-store-provider.md)

