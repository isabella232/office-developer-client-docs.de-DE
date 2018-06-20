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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 31b2353b76bbac5cd58cd791f4a289c7dbabdb78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793109"
---
# <a name="mapiinit0"></a>MAPIINIT_0

  
  
**Betrifft**: Outlook 
  
Optionen für die Funktion ["MAPIInitialize"](mapiinitialize.md) übermittelt. 
  
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

## <a name="members"></a>Members

 **ulVersion**
  
> Ein Ganzzahlwert, der die Versionsnummer der **MAPIINIT_0** Struktur darstellt. Das **UlVersion** -Element ist für die zukünftige Erweiterung und die Version der MAPI-Schnittstelle stellt keine dar. Derzeit muss **UlVersion** auf MAPI_INIT_VERSION festgelegt sein. 
    
 **ulFlags**
  
> Die Bitmaske Flags verwendet, um die Initialisierung der MAPI-Sitzung zu steuern. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI sollte mit einem Thread dedizierte Benachrichtigung anstelle des ersten Threads verwendet, um das Aufrufen von **"MAPIInitialize"** Behandeln von Benachrichtigungen generieren.
    
MAPI_NT_SERVICE 
  
> Der Anrufer wird als Windows-Dienst ausgeführt. Anrufer, die wie ein Windows-Dienst nicht dieses Flag festlegen sollten nicht ausgeführt werden; Anrufer, die als Dienst ausgeführt werden, müssen dieses Flag festgelegt.
    
MAPI_NO_COINIT
  
> Das Flag MAPI_NO_COINT so festgelegt, dass **"MAPIInitialize"** nicht versucht, mit einem Aufruf von [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)COM initialisieren. Wenn eine **MAPIINIT_0** -Struktur mit _UlFlags_ auf MAPI_NO_COINIT festgelegt in **"MAPIInitialize"** übergeben wird, wird MAPI wird vorausgesetzt, dass COM bereits initialisiert wurde, und den Aufruf von **CoInitialize**umgangen wird.
    
## <a name="remarks"></a>Hinweise

Multithread-Clients sollte das MAPI_MULTITHREAD_NOTIFICATIONS Flag festgelegt. Wenn das Flag nicht festgelegt ist, werden Benachrichtigungen auf dem Thread verwendet, um den ersten Aufrufen **"MAPIInitialize"** generiert. 
  
Weitere Informationen, wann dieses Flag festgelegt und wie Threadsicherheit in einer Clientdatenbank implementieren finden Sie unter [Threading in MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Siehe auch



["MAPIInitialize"](mapiinitialize.md)


[MAPI-Strukturen](mapi-structures.md)

