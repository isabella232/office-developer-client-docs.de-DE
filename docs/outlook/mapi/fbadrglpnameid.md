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
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434830"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft ein Array von Strukturen, die benannte Eigenschaften beschreiben, und überprüft deren Zuordnung. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
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
  
> [in] Zeiger auf ein Array von [MAPINAMEID-Strukturen,](mapinameid.md) die die benannten Eigenschaften beschreiben. 
    
 _cNames_
  
> [in] Anzahl der benannten Eigenschaftenstrukturen im Array, auf die der  _lppNameId-Parameter_ verweist. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Mindestens eine der angegebenen Eigenschaftennamensstrukturen ist ungültig. 
    
FALSE 
  
> Die angegebenen Eigenschaftennamensstrukturen sind alle gültig.
    
## <a name="remarks"></a>Hinweise

Die **FBadRglpNameID-Funktion** kann beim Einrichten eines Aufrufs von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) oder [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)verwendet werden. 
  

