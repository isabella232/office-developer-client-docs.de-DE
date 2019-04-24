---
title: IMAPIFormInfoOpenFormContainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a76d0c554d7cf06aceeaa2925c199e45411b999d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342091"
---
# <a name="imapiforminfoopenformcontainer"></a>IMAPIFormInfo::OpenFormContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf den Formular Container zurück, in dem ein bestimmtes Formular installiert ist.
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a>Parameter

 _ppformcontainer_
  
> Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular Container-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

