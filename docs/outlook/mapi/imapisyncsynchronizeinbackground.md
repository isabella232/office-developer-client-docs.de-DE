---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Zuletzt geändert: 26 Juni 2012'
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792442"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync: SynchronizeInBackground

 
  
**Betrifft**: Outlook 
  
 Initiiert eine Synchronisierung. Diese Methode wird von Microsoft Outlook 2010 und Microsoft Outlook 2013 aufgerufen und Zeichenfolgeneigenschaften Nachricht implementiert. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Parameter

 _psibpb_
  
> Informiert den Anbieter von Was synchronisiert werden soll, und ermöglicht den Zugriff auf Schnittstellen, die während der Synchronisierung verwendet werden können. Es ist eine [MAPISIB](mapisib.md) -Struktur. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISync: IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

