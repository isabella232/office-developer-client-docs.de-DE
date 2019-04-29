---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415131"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die Liste der Registrierungen für die persönliche Ordner-Datei (PST) ab.
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parameter

 _ppmval_
  
> in Ein Zeiger auf einen Zeiger auf eine [SPropValue](spropvalue.md) -Struktur. Das ulPropTag-Element dieser Struktur hat den Typ PT_MV_UNICODE, und der MVszW-Wert Member ist ein Array von null-terminierten Unicode-Zeichenfolgen. Diese Zeichenfolgen sind Pfade zu DLLs, für die die Registrierung beibehalten wurde. 
    
> [!NOTE]
> die PST-Unterstützung für ANSI ist nicht implementiert. 
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

