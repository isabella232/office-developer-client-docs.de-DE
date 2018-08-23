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
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575868"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft die Liste von Einträgen für den persönlichen Ordner (PST) Datei ab.
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parameter

 _ppmval_
  
> [in] Ein Zeiger auf einen Zeiger auf eine [SPropValue](spropvalue.md) -Struktur. Der Member UlPropTag diese Struktur ist vom Typ PT_MV_UNICODE, und das MVszW Element wird ein Array mit Null terminierte Unicode-Zeichenfolgen sein. Diese Zeichenfolgen sind Pfade zu DLLs für die Registrierung beibehalten wurde. 
    
> [!NOTE]
> Unterstützung von ANSI PST-Dateien ist nicht implementiert. 
  
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

