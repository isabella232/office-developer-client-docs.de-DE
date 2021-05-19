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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420591"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ersetzt [MAPIInitialize,](mapiinitialize.md) wenn nur ausgewählte Hilfsfunktionen verwendet werden. 
  
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
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Die **Funktionen ScInitMapiUtil** und [DeinitMapiUtil](deinitmapiutil.md) arbeiten zusammen, um ausgewählte Hilfsfunktionen auf- und frei zu geben, im Gegensatz zu [MAPIInitialize](mapiinitialize.md), das Kern- und Hilfsfunktionen aufruft. Wenn **ScInitMapiUtil** Hilfsfunktionen aufruft, initialisiert es auch den erforderlichen Arbeitsspeicher. 
  
Wenn die Verwendung der Funktionen, die **ScInitMapiUtil** aufgerufen hat, abgeschlossen ist, **muss DeinitMapiUtil** explizit aufgerufen werden, um sie frei zu geben. Im Gegensatz dazu ruft **MAPIInitialize** implizit **DeinitMapiUtil auf.** 
  
## <a name="see-also"></a>Siehe auch



[MAPIUninitialize](mapiuninitialize.md)

