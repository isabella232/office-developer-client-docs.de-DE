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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792786"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Betrifft**: Outlook 
  
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

