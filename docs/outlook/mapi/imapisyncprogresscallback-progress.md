---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341258"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktualisiert den Status im Dialogfeld senden/empfangen. Der Informationsspeicher Anbieter ruft diese Funktion regelmäßig auf.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Parameter

 **pwczsProgress**
  
> Ein Zeiger auf eine Zeichenfolge, die den aktuellen Status Schritt anzeigt. Es kann NULL sein, um den Fortschritt zu aktualisieren.
    
 **ulIndex**
  
> Aktuelle Position.
    
 **ulIndexMax**
  
> Der Index, der den vollständigen Fortschritt angibt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

