---
title: Programmgesteuertes Festlegen der Auflösungsreihenfolge für Adresslisten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f9559afb-8db1-ce72-3e11-9b3d47bb80b6
description: 'Zuletzt geändert: 06 Juli, 2012'
ms.openlocfilehash: 4ca3e9d11a3133236d38ef31b01ecded932e8013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345962"
---
# <a name="programmatically-set-the-resolution-order-for-address-lists"></a>Programmgesteuertes Festlegen der Auflösungsreihenfolge für Adresslisten
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das die Reihenfolge von Adresslisten programmgesteuert festlegt, nach der Empfänger in e-Mail-Nachrichten und Teilnehmern in Besprechungsanfragen aufgelöst werden.
  
In MAPI kann jedes Profil mehrere Adresslisten unterstützen, und jede Adressliste befindet sich in einem eigenen Container. MAPI unterstützt die **[SetSearchPath](https://support.microsoft.com/kb/292590)** -Methode in der Schnittstelle, mit der Sie einen neuen Suchpfad im Profil festlegen können, das für die Namensauflösung verwendet wird. Um die **IAddrBook:: SetSearchPath** -Methode verwenden zu können, müssen Sie die gewünschte Auflösungsreihenfolge in einem **[SRowSet](srowset.md)** -Array definieren, in dem die Container der relevanten Adressbücher in der gewünschten Reihenfolge enthalten sind, und dann das Array als *lpSearchPath*  Parameter. Die erste Eigenschaft für jeden Eintrag im **SRowSet** -Array muss die **[PR_ENTRYID](pidtagentryid-canonical-property.md)** -Eigenschaft des entsprechenden Adressbuchs sein. 
  
Im Codebeispiel wird die Auflösungsreihenfolge in den folgenden Schritten festgelegt:
  
1. Initialisiert `numANR` die Anzahl der übereinstimmenden Container und gibt die Namen und die Auflösungsreihenfolge der gewünschten Adresslisten in `ANROrder` einem Array an. 
    
2. Initialisiert MAPI mithilfe der **MAPIInitialize** -Funktion. 
    
3.  Meldet sich bei MAPI an und ermöglicht es dem Benutzer, ein Profil auszuwählen. 
    
4.  Ruft einen Zeiger auf das Adressbuch aus der aktuellen Sitzung ab. 
    
5. Öffnet das Adressbuch.
    
6. Öffnet den Container für das Stamm Adressbuch.
    
7. Öffnet die Hierarchietabelle des Stamm Adressbuch-Containers.
    
8. Ruft die Liste der Adressbuchcontainer in der Hierarchie ab.
    
9. Sucht nach den Eintrags-IDs der gewünschten Adresslisten, indem die Namen der gewünschten Adresslisten in `ANROrder` den vorhandenen Namen in der Adressbuchhierarchie verglichen werden. 
    
10. Legt die entsprechenden Eintrags-IDs **** auf das SRowSet `pNewRows`-Array fest.
    
11. Aufrufe und übergibt `pNewRows` als *lpSearchPath* -Parameter an **IAddrBook:: SetSearchPath** , um den Suchpfad festzulegen. 
    
12. Bereinigt interne Puffer und Zeiger.
    
13. Meldet sich von MAPI ab.
    
14. Uninitalizes MAPI.
    
In diesem Codebeispiel werden Adresslisten verwendet, die in der Standardinstallation von Microsoft Office Outlook verfügbar sind: **alle Kontakte**, **alle Gruppen**und **Kontakte**. Sie müssen das Beispiel ausführen, nachdem Outlook gestartet wurde und in einem initialisierten Profil ausgeführt wird. Das Beispiel funktioniert gut mit Namen, die sich in einer Sprache befinden (beispielsweise sind alle Namen in Englisch). Es ist nicht für die Verwendung in mehrsprachigen Bereitstellungen vorgesehen, beispielsweise für den Ordner " **Kontakte** ", der für einen Benutzer mit einem nicht-englischen Outlook-Build lokalisiert wurde. 
  
```cpp
#include "stdafx.h" 
#include <mapix.h> 
#include <mapiguid.h> 
#include <mapiutil.h> 
#include <mapidefs.h> 
#include <stdio.h> 
#include <conio.h> 
 
//Number of address lists to resolve against 
const int numANR = 3; 
WCHAR *ANROrder[numANR] = {_T("All Contacts"), _T("All Groups"), _T("Contacts")}; 
UINT  numContainersFound [numANR] = {0}; 
 
// Temporary structure to allocate buffer in MAPI. This will be used as a parent buffer to free space later. 
LPVOID tempLink; 
 
// Forward declaration of helper function to copy binary data 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent); 
 
void main() 
{ 
    // MAPI address book and session variables 
    HRESULT       hRes = S_OK;            // Result code returned from MAPI calls. 
    LPMAPISESSION lpSession = NULL;   // Pointer to MAPI session. 
    LPADRBOOK     lpAddrBook = NULL;  // Pointer to Address Book. 
 
    // Counters 
    ULONG         i = 0;                  // Index counter 
    ULONG         j = 0;                  // Index counter 
 
    // Used for querying hierarchy 
    ULONG                                   ulObjType = 0L;      // Object type returned by MAPI 
    LPMAPICONTAINER     pIABRoot = NULL;     // Root address book container 
    LPMAPITABLE              pHTable = NULL;      // Holds hierarchy table 
    LPSRowSet        pRows = NULL;        // Pointer to row set. Stores AB Address Lists 
 
    // Used for setting search path 
    LPSRowSet     pNewRows = NULL;        // Pointer to new row set 
    SizedSRowSet  (numANR, NewRows);      // New row set 
    SPropValue    sProps[numANR] = {0};   // Property tag structure 
 
    // Structures contaning MAPI Column Sets required for querying tables 
    enum { 
        abPR_ENTRYID, 
        abPR_DISPLAY_NAME_W, 
        abNUM_COLS}; 
 
    static SizedSPropTagArray(abNUM_COLS,abCols) = { 
        abNUM_COLS, 
        PR_ENTRYID, 
        PR_DISPLAY_NAME_W, 
    }; 
 
    // Initialize MAPI 
    if (FAILED ( hRes = MAPIInitialize(NULL))) goto Exit; 
 
    // Log on to MAPI and allow user to choose profile 
 
    // Note: This uses the current MAPI session if there is one 
    if (FAILED ( hRes = MAPILogonEx(NULL, NULL, NULL, MAPI_LOGON_UI, &lpSession))) goto Exit; 
 
    // Open the Address Book 
    if (FAILED (hRes = lpSession->OpenAddressBook(NULL, NULL, NULL, &lpAddrBook))) goto Cleanup; 
 
    // Open the Address Book Root container 
    if (FAILED (hRes = lpAddrBook -> OpenEntry ( 
        0L,  
        NULL, 
        NULL,  
        0L, 
        &ulObjType, 
        (LPUNKNOWN *) &pIABRoot ))) 
    goto Cleanup; 
 
    // Intentionally allocate 0 bytes. This is used for buffer management. 
    MAPIAllocateBuffer(0L, &tempLink);  
 
    // Make sure there is a Container object 
    // Query hierarchy for containers 
    if ( MAPI_ABCONT == ulObjType ) { 
        // - Call IMAPIContainer::GetHierarchyTable to open the Hierarchy 
        //   table of the root address book container 
        if ( FAILED ( hRes = pIABRoot -> GetHierarchyTable ( CONVENIENT_DEPTH | MAPI_UNICODE, 
            &pHTable ) ) ) 
        goto Cleanup; 
 
        // Get the list of address book containers first 
        if ( FAILED ( hRes = HrQueryAllRows (  
            pHTable, 
            (LPSPropTagArray) &abCols, 
            NULL, 
            NULL, 
            0L, 
            &pRows ) ) ) 
        goto Cleanup; 
 
        // Initialize the structures to set the search order 
        ZeroMemory(&NewRows, numANR * sizeof(SRow)); 
        pNewRows = (LPSRowSet)&NewRows; 
 
        // Set the number of rows you are going to set 
        pNewRows->cRows = numANR; 
 
        // Set the pointers to the structures 
        for (i=0; i<numANR; i++) 
            pNewRows->aRow[i].lpProps = &sProps[i]; 
 
        // Compare the list to the ones that of interest 
        for (i=0; i<pRows->cRows; i++) { 
            if (pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].ulPropTag == PR_DISPLAY_NAME_W) { 
                LPWSTR containerName =  pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].Value.lpszW; 
                for (j=0; j<numANR; j++) 
                    if (!wcscmp (containerName, ANROrder[j])) { 
                        // First check if a container with this name has been found already 
                        if (numContainersFound[j] == 0) { 
                            numContainersFound[j]++; 
                            pNewRows->aRow[j].cValues = 1; 
 
                            // The property being passing is PR_ENTRY_ID 
                            pNewRows->aRow[j].lpProps[0].ulPropTag = PR_ENTRYID; 
 
                            // Copy the binary data over 
                            if (FAILED (hRes = CopySBinary( 
                                &pNewRows->aRow[j].lpProps[0].Value.bin, 
                                &pRows->aRow[i].lpProps[abPR_ENTRYID].Value.bin, 
                                tempLink))) {  
                                    printf ("Fatal Error:Failed to copy entry IDs\n"); 
                                    goto Cleanup; 
                            } 
                         } 
                         // More than 1 container matched the same name 
                         else {  
                             printf ("Fatal Error: Duplicate container found, container name = %s\n", containerName); 
                             goto Cleanup; 
                         } 
                    } 
            } 
        } 
 
        // Only set the search path if all the rows have been found 
        // Check the array for any entries that were blank 
        for (i=0; i< numANR; i++) 
            if (numContainersFound [i] == 0) { 
                printf ("Fatal Error: all containers were not found\n"); 
                goto Cleanup; 
            } 
 
        // Everything is safe to set the search path now 
        if (FAILED (hRes = lpAddrBook->SetSearchPath(0, pNewRows))) {                    
            printf ("Fatal Error: failed to set the search path\n"); 
            goto Cleanup; 
        } 
    } 
 
    Cleanup: 
        MAPIFreeBuffer(tempLink); 
        UlRelease(pHTable); 
        FreeProws(pRows); 
        UlRelease (pIABRoot); 
        UlRelease(lpAddrBook); 
 
        // Log off from MAPI 
        hRes = lpSession->Logoff(NULL, NULL, 0); 
        UlRelease(lpSession); 
 
    Exit: 
        // Uninitialize MAPI 
        MAPIUninitialize(); 
} 
 
///////////////////////////////////////////////////////////// 
//    CopySBinary() 
// 
//    Parameters 
// 
//    Purpose 
//      Allocates a new SBinary and copies psbSrc into it 
// 
 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent) 
{ 
    HRESULT     hRes = S_OK; 
    psbDest->cb = psbSrc->cb; 
 
    if (psbSrc->cb) { 
        if (pParent) 
            hRes = MAPIAllocateMore( 
                 psbSrc->cb, 
                 pParent, 
                 (LPVOID*) &psbDest->lpb); 
        else 
            hRes = MAPIAllocateBuffer( 
                 psbSrc->cb, 
                 (LPVOID*) &psbDest->lpb); 
 
    if (!FAILED(hRes)) 
        CopyMemory(psbDest->lpb,psbSrc->lpb,psbSrc->cb); 
    } 
 
   return hRes; 
} 

```

## <a name="see-also"></a>Siehe auch

- [Informationen zum Festlegen der aufLösungsReihenfolge für Adresslisten in Outlook](about-setting-the-resolution-order-for-address-lists-in-outlook.md)

