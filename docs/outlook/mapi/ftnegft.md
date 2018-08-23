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
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589238"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Berechnet die beiden Komplement eine 64-Bit-Ganzzahl ohne Vorzeichen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Parameter

 _FT_
  
> [in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen für die die beiden Ergänzung berechnet enthält. 
    
## <a name="return-value"></a>R�ckgabewert

Die **FtNegFt** -Funktion gibt eine **FILETIME** -Struktur, die die beiden Ergänzung der ganzen Zahl enthält. Der Eingabeparameter bleibt unverändert. 
  

