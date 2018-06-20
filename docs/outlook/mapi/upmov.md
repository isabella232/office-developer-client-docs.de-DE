---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 43fd56932409861db86679eea6f1405dc4c37e62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795810"
---
# <a name="upmov"></a>UPMOV
 
**Betrifft**: Outlook 
  
Informationen zum Hochladen von Elementen, die verschoben wurden. Diese Informationen werden während der [Upload löschen Status Zustand](upload-delete-status-state.md) und [Status Tabelle hochladen](upload-table-state.md)verwendet.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [in] Kennzeichen, die um das entsprechende Verhalten beim Hochladen zu bestimmen.
    
  - UPV_ERROR
    
    - [in] Problem beim Öffnen von Serverordner.
    
  - UPV_DIRTY
    
    - [in] Der Upload-Status hat sich geändert. Dies wird vom Client verwendet, um die Änderung im Zustand für den lokalen Speicher zu verfolgen.
    
  - UPV_COMMIT
    
    - [in] Commit Upload Zustand.
    
_Beibehalten_
  
>  [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pstmReserved_
  
>  [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pszName_
  
>  [out] Name des Zielordners. 
    
  > [!NOTE]
  > Dieser Member wird UNICODE nicht unterstützt. 
  
_feid_
  
>  [out] Eintrags-ID der Zielordner. 
    
_pfld_
  
>  [in] Zeiger auf den Ordner auf dem Server. 
    
_pxicc_
  
>  [in] Zeiger auf die Schnittstelle der **IExchangeImportContentsChanges** -Inhalt, die Hochladen von Änderungen bei Verwendung von inkrementelle Änderung Synchronisierung (ICS) unterstützt. Weitere Informationen zu **IExchangeImportContentsChanges** und ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
>  [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pupmovNext_
  
>  [out] Als Nächstes Kontext zu verschieben. 
    
_cEntMov_
  
>  [in] Anzahl der Elemente hier verschoben. 
    
## <a name="see-also"></a>Siehe auch

- [Über die API-Replikation](about-the-replication-api.md)
- [Informationen zu den Replikationsstatus Computer](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [FEID](feid.md)

