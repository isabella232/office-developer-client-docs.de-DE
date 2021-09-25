---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 1106df7e7d0926f9a7a4d4d1f0d1425f1bf11371
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556763"
---
# <a name="dntbl"></a>DNTBL
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Herunterladen der Inhalte eines Ordners vom Server während des [Download-Tabellenzustands](download-table-state.md) als Teil einer vollständigen Synchronisierung für Inhalte in einem Speicher.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a>Elemente

_ulFlags_
  
> [in] Flags, die Verhalten ändern. 
    
  - DNT_OK
    
    - [in] Download war erfolgreich. Der Client legt dies nach dem Herunterladen von Informationen vom Server fest.
    
_pstmReserved1_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pstmReserved2_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pstmReserved3_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pstmReserved4_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pxicc_
  
>  [out] Verweis auf die **IExchangeImportContentsChanges**-Inhaltsschnittstelle, die das Herunterladen von Änderungen unterstützt. Weitere Informationen zu **IExchangeImportContentsChanges** finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pxihc_
  
>  [out] Verweis auf die **IExchangeImportHierarchyChanges**-Hierarchieschnittstelle, die das Herunterladen von inkrementellen Hierarchieänderungen unterstützt. Weitere Informationen zu **IExchangeImportHierarchyChanges** finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pszName_
  
>  [out] Der Name des Ordners. 
    
_ftLastMod_
  
>  [out] Uhrzeit der letzten Änderung des Ordners. 
    
_ulRights_
  
>  [out] Der Wert der **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)**-Eigenschaft des Ordners. 
    
_feid_
  
>  [out] Eintrags-ID des Ordners. 
    
_uintReserved_
  
>  [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_rgte_
  
> [out] Änderungen für normale (oder nicht ausgeblendet) und verknüpfte (oder ausgeblendeten) Elemente.  *rgte[0]*  ist für normale Elemente, *rgte[1]* ist für verknüpfte Elemente. Outlook füllt dieses Element während des Herunterladens bei Verwendung von Incremental Change Synchronization (ICS) auf. Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_lpsrReserved_
  
>  [in]/[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_boReserved_
  
>  [in] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pReserved1_
  
>  [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pReserved2_
  
>  [in] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)  
- [MAPI-Konstanten](mapi-constants.md) 
- [DNTBLE](dntble.md)

