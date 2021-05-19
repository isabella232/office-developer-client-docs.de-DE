---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416972"
---
# <a name="smapiforminfoarray"></a>SMAPIFormInfoArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeigern zu Formularinformationsobjekten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verwandtes Makro:  <br/> |[CbMAPIFormInfoArray](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a>Elemente

 **cForms**
  
> Anzahl der Zeiger im Array, auf die das **Element aFormInfo verweist.** 
    
 **aFormInfo**
  
> Zeiger auf ein Array von Zeigern, um Informationsobjekte zu bilden.
    
## <a name="remarks"></a>Hinweise

Die **SMAPIFormInfoArray-Struktur** wird in den folgenden Methoden als Parameter übergeben: 
  
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormMgr::SelectMultipleForms](imapiformmgr-selectmultipleforms.md)
    
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

