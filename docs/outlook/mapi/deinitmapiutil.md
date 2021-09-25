---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 70d6365ed2f1b38da7759c4d872c25358dc927d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556812"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Hilfsfunktionen frei, die explizit von der [ScInitMapiUtil-Funktion](scinitmapiutil.md) oder implizit von der [MAPIInitialize-Funktion](mapiinitialize.md) aufgerufen werden. 
  
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
  
## <a name="return-value"></a>Rückgabewert

Keines 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Freigabefunktionen für die **Funktion "FunktionsfähigeItMapiUtil"** werden mit [ScInitMapiUtil](scinitmapiutil.md) oder [MAPIInitialize initialisiert.](mapiinitialize.md) 
  
Wenn die Verwendung der von **ScInitMapiUtil** aufgerufenen Funktionen abgeschlossen ist, muss **Dies** explizit aufgerufen werden, um sie freizugeben. Im Gegensatz dazu ruft [MAPIUninitialize](mapiuninitialize.md) implizit **ObjekteitMapiUtil** auf. 
  

