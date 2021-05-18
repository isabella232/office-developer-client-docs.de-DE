---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412695"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeigern auf Nachrichtenklassenzeichenfolgen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verwandtes Makro:  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Zeichenfolgenzeiger der Nachrichtenklasse im Array.
    
 **aMessageClass**
  
> Array von Zeigern auf Nachrichtenklassenzeichenfolgen.
    
## <a name="remarks"></a>Hinweise

Die **SMessageClassArray-Struktur** wird in den folgenden Methoden als Parameter übergeben: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

