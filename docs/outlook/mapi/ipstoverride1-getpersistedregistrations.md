---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 397eb3ecfeb245a6afe91be98a5def4c35ba4873
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579754"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die Liste der Registrierungen für die Datei "Persönliche Ordner" (PST) ab.
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parameter

 _ppmval_
  
> [in] Ein Zeiger auf einen Zeiger auf eine [SPropValue-Struktur.](spropvalue.md) Das ulPropTag-Element dieser Struktur hat den Typ PT_MV_UNICODE, und der MVszW-Wertmember ist ein Array von Unicode-Zeichenfolgen, die mit Null terminiert sind. Diese Zeichenfolgen sind Pfade zu DLLs, für die die Registrierung beibehalten wurde. 
    
> [!NOTE]
> PST-Unterstützung für ANSI ist nicht implementiert. 
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

