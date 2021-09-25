---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6dbc027dfc3dfb2a0b4cf3a0096c5d33e5b4d4a0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591213"
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Funktionen **ScInitMapiUtil** und [DropdownitMapiUtil](deinitmapiutil.md) arbeiten zusammen, um ausgewählte Hilfsfunktionen aufzurufen und freizugeben, im Gegensatz zu [MAPIInitialize](mapiinitialize.md), die Sowohl Kern- als auch Hilfsfunktionen aufruft. Wenn **ScInitMapiUtil** Hilfsfunktionen aufruft, wird auch der erforderliche Speicher initialisiert. 
  
Wenn die Verwendung der Funktionen, die **ScInitMapiUtil** aufgerufen hat, abgeschlossen ist, muss **Dies** explizit aufgerufen werden, um sie freizugeben. Im Gegensatz dazu ruft **MAPIInitialize** implizit **ObjekteitMapiUtil** auf. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUninitialize](mapiuninitialize.md)

