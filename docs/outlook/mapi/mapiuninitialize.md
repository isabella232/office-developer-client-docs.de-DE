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
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567391"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Verringert der Referenzzähler bereinigt, und löscht pro Instanz globale Daten für die MAPI-DLL. 
  
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
  
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung ruft die **MAPIUninitialize** -Funktion, um die Interaktion mit MAPI, mit einem Aufruf der Funktion ["MAPIInitialize"](mapiinitialize.md) begonnen zu beenden. Nachdem **MAPIUninitialize** aufgerufen wurde, können keine anderen MAPI-Aufrufe vom Client vorgenommen werden. 
  
 **MAPIUninitialize** den Referenzzähler und die entsprechende **"MAPIInitialize"** Funktion erhöht den Referenzzähler. Die Anzahl der Anrufe an eine Funktion muss daher die Anzahl der Aufrufe der anderen entsprechen. 
  
> [!NOTE]
> **"MAPIInitialize"** oder **MAPIUninitialize** aus kann nicht innerhalb einer Win32 **DllMain** -Funktion oder eine andere Funktion, die erstellt oder Threads beendet aufgerufen werden. Weitere Informationen finden Sie unter [Verwenden von threadsicheren Objekten](using-thread-safe-objects.md). 
  

