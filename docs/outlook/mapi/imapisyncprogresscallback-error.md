---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d70dc611a7756c8dca15e1c173e5702a7fc86f63
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575750"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Details bereit, die im Dialogfeld "Senden/Empfangen" angezeigt werden. Wenn während der Synchronisierung Fehler auftreten, ruft der Speicheranbieter diese Funktion auf.
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>Parameter

 **Hresult**
  
> Das HRESULT des Fehlers oder der Warnung.
    
 **pwcszErrorStr**
  
> Ein Zeiger auf die Zeichenfolge, die dem anzuzeigenden Fehler zugeordnet ist.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

