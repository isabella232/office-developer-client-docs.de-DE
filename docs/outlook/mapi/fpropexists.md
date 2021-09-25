---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dada6f5c1e9ddce388901d359766fe9a80c08f45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551576"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach einem bestimmten Eigenschaftentag in einer [IMAPIProp-Schnittstelle](imapipropiunknown.md) oder einer von **IMAPIProp** abgeleiteten Schnittstelle, z. B. [IMessage](imessageimapiprop.md) oder [IMAPIFolder.](imapifolderimapicontainer.md) 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameter

 _pobj_
  
> [in] Zeiger auf die VON IMAPIProp abgeleitete **IMAPIProp-Schnittstelle** oder -Schnittstelle, innerhalb derer nach dem Eigenschaftentag gesucht werden soll.  
    
 _ulPropTag_
  
> [in] Eigenschaftentag, nach dem gesucht werden soll.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Es wurde eine Übereinstimmung für das angegebene Eigenschaftstag gefunden. 
    
FALSE 
  
> Eine Übereinstimmung für das angegebene Eigenschaftstag wurde nicht gefunden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das Eigenschaftstag im  _ulPropTag-Parameter_ den Typ PT_UNSPECIFIED aufweist, sucht die **FPropExists-Funktion** nur basierend auf dem Eigenschaftsbezeichner nach einer Übereinstimmung. Andernfalls gilt die Übereinstimmung für das gesamte Eigenschaftstag, einschließlich des Typs. 
  

