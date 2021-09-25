---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e06dfe806ca3d99f35a369eb4a7cf6fe8da50717
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551128"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verringert die Anzahl der Verweise, bereinigt und löscht die globalen Daten pro Instanz für die MAPI-DLL. 
  
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung ruft die **MAPIUninitialize-Funktion** auf, um ihre Interaktion mit der MAPI zu beenden, und beginnt mit einem Aufruf der [MAPIInitialize-Funktion.](mapiinitialize.md) Nachdem **MAPIUninitialize** aufgerufen wurde, können keine weiteren MAPI-Aufrufe vom Client ausgeführt werden. 
  
 **MAPIUninitialize** verringert die Referenzanzahl, und die entsprechende **MAPIInitialize-Funktion** erhöht die Referenzanzahl. Daher muss die Anzahl der Aufrufe einer Funktion mit der Anzahl der Aufrufe an die andere Funktion übereinstimmen. 
  
> [!NOTE]
> Sie können **MAPIInitialize** oder **MAPIUninitialize** nicht innerhalb einer Win32 **DllMain-Funktion** oder einer anderen Funktion aufrufen, die Threads erstellt oder beendet. Weitere Informationen finden Sie unter [Using Thread-Safe Objects](using-thread-safe-objects.md). 
  

