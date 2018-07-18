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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791505"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Betrifft**: Outlook 
  
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
  

