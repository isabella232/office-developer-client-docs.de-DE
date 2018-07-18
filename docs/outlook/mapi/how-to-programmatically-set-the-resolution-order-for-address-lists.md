---
title: Die Reihenfolge der Lösung für Adresslisten programmgesteuert festlegen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f9559afb-8db1-ce72-3e11-9b3d47bb80b6
description: 'Zuletzt geändert: 06 Juli 2012'
ms.openlocfilehash: 676d74c6441716203006f2db3e4a7d5777320a98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791869"
---
# <a name="programmatically-set-the-resolution-order-for-address-lists"></a>Die Reihenfolge der Lösung für Adresslisten programmgesteuert festlegen
  
**Betrifft**: Outlook 
  
Dieses Thema enthält ein Codebeispiel in C++, die die Reihenfolge der Adresslisten programmgesteuert festlegt, durch welche Empfänger in e-Mail-Nachrichten und Teilnehmer in Besprechungsanfragen aufgelöst werden.
  
In MAPI jedes Profil kann mehrere Adresslisten unterstützen, und jede Adressliste befindet sich in einem eigenen Container. MAPI unterstützt die **[SetSearchPath](http://support.microsoft.com/kb/292590)** -Methode auf der Benutzeroberfläche, mit dem Sie einen neuen Pfad für die Suche im Profil festlegen, die für die namensauflösung verwendet wird. Um die **IAddrBook::SetSearchPath** -Methode verwenden, müssen Sie die gewünschte Auflösung Reihenfolge in einem Array **[SRowSet](srowset.md)** definieren, die die Container der relevanten Adressbücher in der gewünschten Reihenfolge enthält, und legen Sie das Array als die *lpSearchPath*  der Parameter. Die erste Eigenschaft für jeden Eintrag im Array **SRowSet** muss die **[PR_ENTRYID](pidtagentryid-canonical-property.md)** -Eigenschaft des entsprechenden Adressbuch. 
  
Im Codebeispiel wird die Lösung in den folgenden Schritten:
  
1. Initialisiert `numANR` auf die Anzahl der Container übereinstimmen, und gibt den Namen und die Lösung Reihenfolge der gewünschten Adresslisten in einer `ANROrder` Array. 
    
2. Initialisiert MAPI mithilfe der Funktion **"MAPIInitialize"** . 
    
3.  Meldet sich bei MAPI und ermöglicht es dem Benutzer ein Profil auswählen. 
    
4.  Ruft einen Zeiger auf das Adressbuch aus der aktuellen Sitzung. 
    
5. Öffnet das Adressbuch.
    
6. Öffnet den Container für den Stamm des Adressbuchs.
    
7. Öffnet die Hierarchietabelle der Stamm Adressbuchcontainer.
    
8. Ruft die Liste der Adresse Adressbuch Container in der Hierarchie.
    
9. Sucht nach die Eintrags-IDs der gewünschten Adresslisten, indem die Namen der gewünschten Adresslisten in Vergleichen `ANROrder` an vorhandenen Namen in der Adressbuchhierarchie. 
    
10. Legt die entsprechenden Eintrags-IDs in das Array **SRowSet** `pNewRows`.
    
11. Ruft auf und übergibt `pNewRows` als Parameter *LpSearchPath* für **IAddrBook::SetSearchPath** Suchpfad festgelegt. 
    
12. Bereinigt die internen Puffer sowie Zeiger.
    
13. Abmeldung von MAPI.
    
14. Uninitalizes MAPI.
    
In diesem Codebeispiel verwendet Adresslisten, die in der standardmäßigen Installation von Microsoft Office Outlook zur Verfügung stehen: **Alle Kontakte**, **Alle Gruppen**und **Kontakte**. Sie müssen das Beispiel ausführen, nachdem Outlook wird gestartet, und klicken Sie auf ein Profil initialisierten ausgeführt wird. Das Beispiel funktioniert auch mit Namen, die in einer Sprache sind (beispielsweise alle Namen sind nur auf Englisch verfügbar). Es ist nicht ausgelegt mehrsprachigen Bereitstellungen, beispielsweise den Ordner **Kontakte** an, der für einen Benutzer, einen nicht - englischen Outlook Build ausgeführt. 
  
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

- [Informationen zum Festlegen der Auflösungsreihenfolge für Adresslisten in Outlook](about-setting-the-resolution-order-for-address-lists-in-outlook.md)

