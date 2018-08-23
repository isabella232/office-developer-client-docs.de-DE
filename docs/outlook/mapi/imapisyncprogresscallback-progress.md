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
ms.openlocfilehash: 5803441486f01883d08cd99048d8eae133cd3f14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592129"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Aktualisiert den Status im Dialogfeld senden/empfangen. Diese Funktion wird in regelmäßigen Abständen Speicheranbieter aufgerufen.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Parameter

 **pwczsProgress**
  
> Ein Zeiger auf eine Zeichenfolge, die den aktuellen Status Schritt wird angezeigt. Zum Aktualisieren des Fortschritts NULL kann sein.
    
 **ulIndex**
  
> Die aktuelle Position in Bearbeitung.
    
 **ulIndexMax**
  
> Der Index, der Fortschritt der Fertigstellung angibt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

