---
title: Öffnen Sie einen Speicher auf dem Remoteserver, wenn Outlook im Exchange-Cache-Modus befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 25f896038e25823f1fe49d3cafbd5835a0a43f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791878"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Öffnen Sie einen Speicher auf dem Remoteserver, wenn Outlook im Exchange-Cache-Modus befindet

**Betrifft**: Outlook 
  
Dieses Thema enthält ein Codebeispiel in C++, die zeigt, wie das Flag **MDB_ONLINE** verwenden, um einen Nachrichtenspeicher auf dem Remoteserver zu öffnen, wenn Microsoft Outlook 2010 oder Microsoft Outlook 2013 im Exchange-Cache-Modus befindet. 
  
Exchange-Cache-Modus ermöglicht Outlook 2010 und Outlook 2013 eine lokale Kopie des Postfachs eines Benutzers zu verwenden, während Outlook 2010 oder Outlook 2013 eine online-Verbindung zu einer remote-Kopie des Postfachs des Benutzers, auf dem Exchange-Remoteserver verwaltet. Wenn Outlook 2010 oder Outlook 2013 standardmäßig im Exchange-Cache-Modus ausgeführt wird werden alle MAPI-Lösungen, die auf der gleichen Sitzung melden Sie sich auch mit den zwischengespeicherten Nachrichtenspeicher verbunden. Anhand der lokalen Kopie des Postfachs werden alle Daten, die zugegriffen werden kann und alle vorgenommenen Änderungen vorgenommen.
  
Ein Client oder Dienstanbieter kann die Verbindung mit den lokalen Nachrichtenspeicher überschreiben und öffnen Sie den Speicher auf dem Remoteserver durch das Bit beim Aufruf von [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)für **MDB_ONLINE** im *UlFlags* -Parameter festlegen. Nachdem Sie der Speicher erfolgreich auf dem Remoteserver für diese Sitzung geöffnet wurde, können Sie [IMAPISession::OpenEntry](imapisession-openentry.md) zum Öffnen von Elementen oder Ordnern auf den remote-Speicher verwenden. 
  
Sie können keinen Exchange-Speicher gleichzeitig in derselben MAPI-Sitzung im Cache-Modus und im nicht-Cache-Modus öffnen. Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie dieses Flag zu öffnen, oder öffnen eine neue MAPI-Sitzung, in dem Sie den Exchange-Speicher auf dem Remoteserver mithilfe dieses Flag öffnen können.
  
Das folgende Codebeispiel zeigt, wie **IMAPISession::OpenMsgStore** aufrufen, mit dem **MDB_ONLINE** -Flag, legen Sie in der *UlFlags* -Parameter auf den Standardinformationsspeicher auf dem Remoteserver zu öffnen. 
  
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
- [Zugreifen auf einen Store auf dem Remote-Server, wenn Outlook sich Exchange-Cache-Modus befindet](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

