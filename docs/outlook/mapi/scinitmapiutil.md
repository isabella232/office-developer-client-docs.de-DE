---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795447"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Betrifft**: Outlook 
  
["MAPIInitialize"](mapiinitialize.md) ersetzt, wenn nur select Hilfsfunktionen verwendet werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Die Funktionen **ScInitMapiUtil** und [DeinitMapiUtil](deinitmapiutil.md) zusammenarbeiten, um aufrufen und Freigeben von select Hilfsfunktionen für Funktionen, im Gegensatz zu ["MAPIInitialize"](mapiinitialize.md), die Core sowie Dienstprogramm aufruft. Wenn **ScInitMapiUtil** Hilfsfunktionen anruft, wird auch den erforderlichen Arbeitsspeicher initialisiert. 
  
Nach Abschluss der Verwendung der Funktionen, die **ScInitMapiUtil** aufgerufen hat muss **DeinitMapiUtil** explizit aufgerufen werden, um diese freigeben. Im Gegensatz dazu ruft **"MAPIInitialize"** implizit **DeinitMapiUtil**. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUninitialize](mapiuninitialize.md)

