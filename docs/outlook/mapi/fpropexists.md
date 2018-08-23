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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570436"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Sucht nach einem bestimmten Eigenschaftentag in eine [IMAPIProp](imapipropiunknown.md) oder einer Schnittstelle abgeleitet **IMAPIProp**wie [IMessage](imessageimapiprop.md) oder [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameter

 _pobj_
  
> [in] Zeiger auf die **IMAPIProp** Schnittstelle oder Schnittstelle abgeleitet **IMAPIProp** innerhalb für das Eigenschafts-Tag gesucht werden soll. 
    
 _ulPropTag_
  
> [in] Eigenschaftentag für gesucht werden soll.
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Eine Übereinstimmung für das Tag für die angegebene Eigenschaft gefunden wurde. 
    
FALSE 
  
> Eine Übereinstimmung für das Tag für die angegebene Eigenschaft wurde nicht gefunden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das Eigenschafts-Tag im Parameter _UlPropTag_ PT_UNSPECIFIED aufweist, sucht die **FPropExists** Funktion für eine Übereinstimmung nur anhand der Eigenschaftenbezeichner. Andernfalls wird die Übereinstimmung für das gesamte Eigenschafts-Tag, einschließlich der Art ein. 
  

