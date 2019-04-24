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
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339186"
---
# <a name="upmov"></a>UPMOV
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Hochladen von Elementen, die verschoben wurden. Diese Informationen werden während des Status [](upload-delete-status-state.md) Status des Uploads und zum [Hochladen von Tabellen](upload-table-state.md)verwendet.
  
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

## <a name="members"></a>Elemente

_ulFlags_
  
> in Flags zum Bestimmen des geeigneten Verhaltens während des Uploads.
    
  - UPV_ERROR
    
    - in Problem beim Öffnen des Serverordners.
    
  - UPV_DIRTY
    
    - in Der Uploadstatus wurde geändert. Dies wird vom Client verwendet, um die Zustandsänderung für den lokalen Speicher nachzuverfolgen.
    
  - UPV_COMMIT
    
    - in Commit-Uploadstatus.
    
_Beibehalten_
  
>  [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pstmReserved_
  
>  [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pszName_
  
>  Out Name des Zielordners. 
    
  > [!NOTE]
  > Dieser Member unterstützt UNICODE nicht. 
  
_feid_
  
>  Out Eintrags-ID des Zielordners. 
    
_pfld_
  
>  in Zeiger auf Serverordner. 
    
_pxicc_
  
>  in Zeiger auf die **IExchangeImportContentsChanges** -Inhalts Oberfläche, die das Hochladen von Inhaltsänderungen unterstützt, wenn die inkrementelle Änderungs Synchronisierung verwendet wird. Weitere Informationen zu **IExchangeImportContentsChanges** und ICS finden Sie unter [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
>  [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pupmovNext_
  
>  Out Nächster Verschiebungs Kontext. 
    
_cEntMov_
  
>  in Die Anzahl der Elemente, die hierhin verschoben wurden. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [FEID](feid.md)

