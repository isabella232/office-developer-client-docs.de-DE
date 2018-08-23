---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574797"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Hilfsfunktionen explizit aufgerufen werden, von der Funktion [ScInitMapiUtil](scinitmapiutil.md) oder implizit von der Funktion ["MAPIInitialize"](mapiinitialize.md) frei. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Parameter

Keine 
  
## <a name="return-value"></a>R�ckgabewert

Keine 
  
## <a name="remarks"></a>Bemerkungen

Die **DeinitMapiUtil** -Funktion Freigabefunktionen mit [ScInitMapiUtil](scinitmapiutil.md) oder ["MAPIInitialize"](mapiinitialize.md)initialisiert. 
  
Nach Abschluss der Verwendung der Funktionen von **ScInitMapiUtil** aufgerufen, muss **DeinitMapiUtil** explizit aufgerufen werden, um diese freigeben. Im Gegensatz dazu ruft [MAPIUninitialize](mapiuninitialize.md) implizit **DeinitMapiUtil**. 
  

