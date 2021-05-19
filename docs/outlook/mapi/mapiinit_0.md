---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357295"
---
# <a name="mapiinit_0"></a>MAPIINIT_0

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Übermittelt Optionen an die [MAPIInitialize-Funktion.](mapiinitialize.md) 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |MAPIX. H  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a>Elemente

 **ulVersion**
  
> Ein ganzzahliger Wert, der die Versionsnummer der MAPIINIT_0 **darstellt.** Das **ulVersion-Element** ist für die zukünftige Erweiterung und stellt nicht die Version der MAPI-Schnittstelle dar. Derzeit muss **ulVersion** auf "MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> Die Bitmaske von Flags, die zum Steuern der Initialisierung der MAPI-Sitzung verwendet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI sollte Benachrichtigungen mithilfe eines Threads generieren, der für die Benachrichtigungsverarbeitung und nicht für den ersten Thread zum Aufrufen von **MAPIInitialize verwendet wird.**
    
MAPI_NT_SERVICE 
  
> Der Anrufer wird als Dienst Windows ausgeführt. Anrufer, die nicht als Dienst Windows, sollten dieses Flag nicht festlegen. Anrufer, die als Dienst ausgeführt werden, müssen dieses Flag festlegen.
    
MAPI_NO_COINIT
  
> Legen Sie MAPI_NO_COINT-Flag fest, damit **MAPIInitialize** nicht versucht, COM mit einem Aufruf von [CoInitialize zu initialisieren.](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx) Wenn eine **MAPIINIT_0** an **MAPIInitialize** übergeben wird und _ulFlags_ auf MAPI_NO_COINIT festgelegt ist, geht MAPI davon aus, dass COM bereits initialisiert wurde und den Aufruf von **CoInitialize umgangen wird.**
    
## <a name="remarks"></a>Hinweise

Multithreadclients sollten das MAPI_MULTITHREAD_NOTIFICATIONS festlegen. Wenn das Flag nicht festgelegt ist, werden Benachrichtigungen für den Thread generiert, der zum ersten Aufruf von **MAPIInitialize verwendet wird.** 
  
Weitere Informationen zum Festlegen dieses Kennzeichens und zum Implementieren der Threadsicherheit in einem Client finden Sie unter [Threading in MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPIInitialize](mapiinitialize.md)


[MAPI-Strukturen](mapi-structures.md)

