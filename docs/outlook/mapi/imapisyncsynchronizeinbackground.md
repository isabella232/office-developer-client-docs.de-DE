---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Letzte Änderung: 26. Juni 2012'
ms.openlocfilehash: 579df1e0dd3b027e8bd4dea832154a4be46f7569
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575757"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Initiiert eine Synchronisierung. Diese Methode wird von Microsoft Outlook 2010 und Microsoft Outlook 2013 aufgerufen und von Nachrichtenspeicheranbietern implementiert. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Parameter

 _psibpb_
  
> Informiert den Anbieter darüber, was synchronisiert wird, und gewährt Zugriff auf Schnittstellen, die während der Synchronisierung verwendet werden können. Es handelt sich um eine [MAPISIB-Struktur.](mapisib.md) 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

