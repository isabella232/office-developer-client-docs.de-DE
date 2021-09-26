---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eeeaff3a4cd3097511c50f8761880c270650eb39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629571"
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Zeichenfolgenzeiger der Nachrichtenklasse im Array.
    
 **aMessageClass**
  
> Array von Zeigern auf Zeichenfolgen der Nachrichtenklasse.
    
## <a name="remarks"></a>Bemerkungen

Die **SMessageClassArray-Struktur** wird in den folgenden Methoden als Parameter übergeben: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

