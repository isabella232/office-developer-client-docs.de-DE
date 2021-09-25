---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 59e299efb01f6af5eacf8358c6ab4cee5c0731a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601008"
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
  
> [in] Anzahl der benannten Eigenschaftenstrukturen im Array, auf das durch den  _Parameter "lppNameId"_ verwiesen wird. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Mindestens eine der angegebenen Eigenschaftennamenstrukturen ist ungültig. 
    
FALSE 
  
> Die angegebenen Eigenschaftennamenstrukturen sind alle gültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadRglpNameID-Funktion** kann beim Einrichten eines Aufrufs von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) oder [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)verwendet werden. 
  

