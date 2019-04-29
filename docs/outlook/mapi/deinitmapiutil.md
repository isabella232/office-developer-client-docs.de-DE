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
  
Gibt die von der [ScInitMapiUtil](scinitmapiutil.md) -Funktion oder implizit von der [MAPIInitialize](mapiinitialize.md) -Funktion aufgerufenen Dienstfunktionen frei. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Parameter

Keine 
  
## <a name="return-value"></a>Rückgabewert

Keine 
  
## <a name="remarks"></a>Bemerkungen

Die **DeinitMapiUtil** -Funktionen werden mit [ScInitMapiUtil](scinitmapiutil.md) oder [MAPIInitialize](mapiinitialize.md)initialisiert. 
  
Wenn die Verwendung der von **ScInitMapiUtil** aufgerufenen Funktionen abgeschlossen ist, muss **DeinitMapiUtil** explizit aufgerufen werden, um Sie zu veröffentlichen. [MAPIUninitialize](mapiuninitialize.md) ruft hingegen implizit **DeinitMapiUtil**auf. 
  

