---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408523"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dekrementiert die Referenzanzahl, bereinigt und löscht die globalen Daten pro Instanz für die MAPI-DLL. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Parameter

Keine 
  
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Eine Clientanwendung ruft die **MAPIUninitialize-Funktion** auf, um die Interaktion mit MAPI zu beenden, die mit einem Aufruf der [MAPIInitialize-Funktion begonnen](mapiinitialize.md) wurde. Nach **dem Aufruf von MAPIUninitialize** können keine weiteren MAPI-Aufrufe vom Client ausgeführt werden. 
  
 **MAPIUninitialize** dekrementiert die Referenzanzahl, und die entsprechende **MAPIInitialize-Funktion** erhöht die Referenzanzahl. Daher muss die Anzahl der Aufrufe einer Funktion der Anzahl der Aufrufe an die andere entspricht. 
  
> [!NOTE]
> Sie können **MAPIInitialize** oder **MAPIUninitialize** nicht innerhalb einer Win32 **DllMain-Funktion** oder einer anderen Funktion aufrufen, die Threads erstellt oder beendet. Weitere Informationen finden Sie unter [Using Thread-Safe Objects](using-thread-safe-objects.md). 
  

