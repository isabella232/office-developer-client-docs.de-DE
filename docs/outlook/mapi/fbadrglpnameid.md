---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96dddc438df67b76f854827eab4dc3e210523243
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588146"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Array von Strukturen, die beschreiben, benannte Eigenschaften überprüft und deren Zuordnung überprüft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Parameter

 _lppNameId_
  
> [in] Zeiger auf ein Array von [MAPINAMEID](mapinameid.md) -Strukturen, die die benannten Eigenschaften beschreiben. 
    
 _cNames_
  
> [in] Anzahl der benannten Eigenschaft Strukturen im Array auf den durch den Parameter _LppNameId_ verwiesen. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Eine oder mehrere der angegebenen Eigenschaft Name Strukturen ist ungültig. 
    
FALSE 
  
> Die angegebene Eigenschaft Name Strukturen sind gültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadRglpNameID** -Funktion kann verwendet werden, wenn für einen Anruf an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) oder [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)einrichten. 
  

