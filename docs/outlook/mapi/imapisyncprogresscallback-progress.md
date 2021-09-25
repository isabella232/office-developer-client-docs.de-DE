---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0f01f495372122c2c2f8b2e5d1242d7a1898f62f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592340"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktualisiert den Status im Dialogfeld "Senden/Empfangen". Diese Funktion wird vom Store-Anbieter regelmäßig aufgerufen.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Parameter

 **pwczsProgress**
  
> Ein Zeiger auf eine Zeichenfolge, die den aktuellen Fortschrittsschritt anzeigt. Es kann NULL sein, um den Fortschritt zu aktualisieren.
    
 **ulIndex**
  
> Die aktuelle Position, die gerade ausgeführt wird.
    
 **ulIndexMax**
  
> Der Index, der den vollständigen Fortschritt angibt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

