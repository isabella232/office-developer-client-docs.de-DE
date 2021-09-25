---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7ffffdae05799ce573beabe1379ff66b059fb63d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616789"
---
# <a name="mapigetdefaultmalloc"></a>MAPIGetDefaultMalloc

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die Adresse der standardmäßigen MAPI-Speicherzuweisungsfunktion ab.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a>Parameter

Keine. 
  
## <a name="return-value"></a>Return value

Die **MAPIGetDefaultMalloc-Funktion** gibt einen Zeiger auf die standardmäßige MAPI-Speicherzuweisungsfunktion zurück. 
  

