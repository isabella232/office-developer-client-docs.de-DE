---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 75aeb9e3c501d3e5c507aad2c832699dbf33edcb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619526"
---
# <a name="upmov"></a>UPMOV
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Hochladen von Elementen, die verschoben wurden. Diese Informationen werden während des Status zum Löschen des [Uploads](upload-delete-status-state.md) und [des Uploadtabellenstatus](upload-table-state.md)verwendet.
  
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
  
> [in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen.
    
  - UPV_ERROR
    
    - [in] Problem beim Öffnen des Serverordners.
    
  - UPV_DIRTY
    
    - [in] Der Uploadstatus wurde geändert. Dies wird vom Client verwendet, um die Statusänderung für den lokalen Speicher nachzuverfolgen.
    
  - UPV_COMMIT
    
    - [in] Uploadstatus übernehmen.
    
_Erhalten_
  
>  [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pstmReserved_
  
>  [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pszName_
  
>  [out] Name des Zielordners. 
    
  > [!NOTE]
  > Unicode wird von diesem Element nicht unterstützt. 
  
_feid_
  
>  [out] Eintrags-ID des Zielordners. 
    
_pfld_
  
>  [in] Zeiger auf Serverordner. 
    
_pxicc_
  
>  [in] Zeiger auf die **IExchangeImportContentsChanges-Inhaltsschnittstelle,** die das Hochladen von Inhaltsänderungen unterstützt, wenn die inkrementelle Änderungssynchronisierung (Incremental Change Synchronization, ICS) verwendet wird. Weitere Informationen zu **IExchangeImportContentsChanges** und ICS finden Sie unter [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_wetterReserved_
  
>  [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_willmovNext_
  
>  [out] Kontext des nächsten Verschiebens. 
    
_cEntMov_
  
>  [in] Die Anzahl der elemente, die hier verschoben wurden. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [FEID](feid.md)

