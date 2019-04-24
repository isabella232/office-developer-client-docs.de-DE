---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327272"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach einem bestimmten Property-Tag in einer [IMAPIProp](imapipropiunknown.md) -Schnittstelle oder einer von **IMAPIProp**abgeleiteten Schnittstelle wie [IMessage](imessageimapiprop.md) oder [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameter

 _pobj_
  
> in Zeiger auf die **IMAPIProp** -Schnittstelle oder-Schnittstelle, die von **IMAPIProp** abgeleitet ist, in der nach dem Property-Tag gesucht werden soll. 
    
 _ulPropTag_
  
> in Eigenschaftentag, nach dem gesucht werden soll.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Eine Übereinstimmung für das angegebene Property-Tag wurde gefunden. 
    
FALSE 
  
> Eine Übereinstimmung für das angegebene Property-Tag wurde nicht gefunden.
    
## <a name="remarks"></a>Bemerkungen

Wenn das Property-Tag im _ulPropTag_ -Parameter den Typ PT_UNSPECIFIED hat, sucht die **FPropExists** -Funktion nach einer Übereinstimmung, die nur auf dem Eigenschaftenbezeichner basiert. Andernfalls ist die Übereinstimmung für das gesamte Property-Tag, einschließlich des Typs. 
  

