---
title: Öffnen eines Speichers auf dem Remoteserver, Outlook sich im Cache-Exchange-Modus befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 419c9ae734e8b58d0958970e7127b94d220b8382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417819"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Öffnen eines Speichers auf dem Remoteserver, Outlook sich im Cache-Exchange-Modus befindet

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, in dem gezeigt wird, wie Sie das **MDB_ONLINE-Flag** verwenden, um einen Nachrichtenspeicher auf dem Remoteserver zu öffnen, wenn Microsoft Outlook 2010 oder Microsoft Outlook 2013 sich im Cached Exchange Mode befindet. 
  
Im cached Exchange Mode können Outlook 2010 und Outlook 2013 eine lokale Kopie des Postfachs eines Benutzers verwenden, während Outlook 2010 oder Outlook 2013 eine Onlineverbindung zu einer Remotekopie des Postfachs des Benutzers auf dem Remoteserver des Exchange verwaltet. Wenn Outlook 2010 oder Outlook 2013 im Cached Exchange Mode ausgeführt wird, sind standardmäßig alle MAPI-Lösungen, die sich bei derselben Sitzung anmelden, auch mit dem zwischengespeicherten Nachrichtenspeicher verbunden. Alle Daten, auf die zugegriffen wird, und alle vorgenommenen Änderungen werden für die lokale Kopie des Postfachs vorgenommen.
  
Ein **Client** oder Dienstanbieter kann die Verbindung zum lokalen Nachrichtenspeicher überschreiben und den Speicher auf dem Remoteserver öffnen, indem er das Bit für MDB_ONLINE im  *ulFlags-Parameter*  beim Aufrufen von [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)festlegen. Nachdem der Speicher auf dem Remoteserver für diese Sitzung erfolgreich geöffnet wurde, können Sie [IMAPISession::OpenEntry](imapisession-openentry.md) verwenden, um Elemente oder Ordner im Remotespeicher zu öffnen. 
  
Sie können einen Exchange im Cachemodus und im nicht zwischengespeicherten Modus nicht gleichzeitig in derselben MAPI-Sitzung öffnen. Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.
  
Im folgenden Codebeispiel wird gezeigt, wie **Sie IMAPISession::OpenMsgStore** mit dem im *ulFlags-Parameter* festgelegten **MDB_ONLINE** aufrufen, um den Standardspeicher auf dem Remoteserver zu öffnen. 
  
```cpp
HRESULT HrRemoteMessageStore( 
    LPMAPISESSION lpMAPISession, 
    LPMDB* lppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMAPITABLE pStoresTbl = NULL; 
    SRestriction sres = {0}; 
    SPropValue spv = {0}; 
    LPSRowSet pRow = NULL; 
    LPMDB lpTempMDB = NULL; 
    enum {EID,NUM_COLS}; 
    static SizedSPropTagArray(NUM_COLS,sptCols) = {NUM_COLS, 
        PR_ENTRYID, 
    }; 
 
    //Obtain the table of all the message stores that are available 
    hRes = lpMAPISession-&gt;GetMsgStoresTable(0, &amp;pStoresTbl); 
     
    if (SUCCEEDED(hRes) &amp;&amp; pStoresTbl) 
    { 
        //Set up restrictions for the default store 
        sres.rt = RES_PROPERTY;                                  //Comparing a property 
        sres.res.resProperty.relop = RELOP_EQ;                   //Testing equality 
        sres.res.resProperty.ulPropTag = PR_DEFAULT_STORE;       //Tag to compare 
        sres.res.resProperty.lpProp = &amp;spv;                      //Prop tag and value to compare against 
     
        spv.ulPropTag = PR_DEFAULT_STORE;                        //Tag type 
        spv.Value.b   = TRUE;                                    //Tag value 
     
        //Convert the table to an array that can be stepped through 
        //Only one message store should have PR_DEFAULT_STORE set to true, so that only one will be returned 
        hRes = HrQueryAllRows( 
            pStoresTbl,                                          //Table to query 
            (LPSPropTagArray) &amp;sptCols,                          //Which columns to obtain 
            &amp;sres,                                               //Restriction to use 
            NULL,                                                //No sort order 
            0,                                                   //Max number of rows (0 means no limit) 
            &amp;pRow);                                              //Array to return 
 
        if (SUCCEEDED(hRes) &amp;&amp; pRow &amp;&amp; pRow-&gt;cRows) 
        {     
            //Open the first returned (default) message store 
            hRes = lpMAPISession-&gt;OpenMsgStore( 
                NULL,                                                //Window handle for dialogs 
                pRow-&gt;aRow[0].lpProps[EID].Value.bin.cb,             //size and... 
                (LPENTRYID)pRow-&gt;aRow[0].lpProps[EID].Value.bin.lpb, //value of entry to open 
                NULL,                                                //Use default interface (IMsgStore) to open store 
                MAPI_BEST_ACCESS | MDB_ONLINE,                       //Flags 
                &amp;lpTempMDB);                                         //Pointer to put the store in 
            if (SUCCEEDED(hRes) &amp;&amp; lppMDB) lppMDB* = lpTempMDB; 
        } 
    } 
    FreeProws(pRow); 
    if (pStoresTbl) pStoresTbl-&gt;Release(); 
 
    return hRes; 
}

```

## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md) 
- [MAPI-Konstanten](mapi-constants.md)
- [Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

