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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341034"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft ein Array von Strukturen, die benannte Eigenschaften beschreiben und deren Zuordnung überprüfen. 
  
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
  
> in Zeiger auf ein Array von [MAPINAMEID](mapinameid.md) -Strukturen, die die benannten Eigenschaften beschreiben. 
    
 _cNames_
  
> in Die Anzahl der benannten Eigenschaftsstrukturen im Array, auf die durch den _lppNameId_ -Parameter verwiesen wird. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Mindestens eine der angegebenen Strukturen für den Eigenschaftennamen ist ungültig. 
    
FALSE 
  
> Die angegebenen Strukturen für den Eigenschaftennamen sind alle gültig.
    
## <a name="remarks"></a>Bemerkungen

Die **FBadRglpNameID** -Funktion kann verwendet werden, wenn Sie einen Aufruf von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) oder [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md)einrichten. 
  

