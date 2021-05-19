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
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427346"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Hilfsfunktionen frei, die explizit von der [ScInitMapiUtil-Funktion](scinitmapiutil.md) oder implizit von der [MAPIInitialize-Funktion aufgerufen](mapiinitialize.md) werden. 
  
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

Keine 
  
## <a name="remarks"></a>Hinweise

Die **Funktionen der DeinitMapiUtil-Funktionsfreigabe** werden mit [ScInitMapiUtil](scinitmapiutil.md) oder [MAPIInitialize initialisiert.](mapiinitialize.md) 
  
Wenn die Verwendung der von **ScInitMapiUtil** aufgerufenen Funktionen abgeschlossen ist, muss **DeinitMapiUtil** explizit aufgerufen werden, um sie frei zu geben. Im Gegensatz dazu ruft [MAPIUninitialize](mapiuninitialize.md) **implizit DeinitMapiUtil auf.** 
  

