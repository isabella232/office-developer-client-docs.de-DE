---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423384"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Berechnet die beiden Komplemente einer unsignierten 64-Bit-Ganzzahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Parameter

 _FT_
  
> in Eine [FILETIME](filetime.md) -Struktur mit der unsignierten 64-Bit-Ganzzahl, für die die Komplemente der beiden berechnet werden sollen. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtNegFt** -Funktion gibt **** eine FILETIME-Struktur zurück, die die Komplemente der ganzen Zahl enthält. Der Eingabeparameter bleibt unverändert. 
  

