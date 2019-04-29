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
description: 'Letzte Änderung: 26. Juni 2012'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426856"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Initiiert eine Synchronisierung. Diese Methode wird von Microsoft Outlook 2010 und Microsoft Outlook 2013 aufgerufen und von Nachrichtenspeicher Anbietern implementiert. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Parameter

 _psibpb_
  
> Informiert den Anbieter darüber, was synchronisiert wird, und gibt Zugriff auf Schnittstellen, die während der Synchronisierung verwendet werden können. Es handelt sich um eine [MAPISIB](mapisib.md) -Struktur. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

