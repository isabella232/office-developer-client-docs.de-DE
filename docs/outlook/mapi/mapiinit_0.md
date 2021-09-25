---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8f94c4b5eac189a672771a91e6b9969462f187ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610125"
---
# <a name="mapiinit_0"></a>MAPIINIT_0

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vermittelt Optionen für die [MAPIInitialize-Funktion.](mapiinitialize.md) 
  
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
  
> Ein ganzzahliger Wert, der die Versionsnummer der **MAPIINIT_0-Struktur** darstellt. Das **ulVersion-Mitglied** ist für zukünftige Erweiterungen vorgesehen und stellt nicht die Version der MAPI-Schnittstelle dar. Derzeit muss **ulVersion** auf MAPI_INIT_VERSION festgelegt werden. 
    
 **ulFlags**
  
> Die Bitmaske der Flags, die zum Steuern der Initialisierung der MAPI-Sitzung verwendet werden. Die folgenden Flags können festgelegt werden:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI sollte Benachrichtigungen mithilfe eines Threads generieren, der der Benachrichtigungsbehandlung zugeordnet ist, anstelle des ersten Threads, der zum Aufrufen von **MAPIInitialize** verwendet wird.
    
MAPI_NT_SERVICE 
  
> Der Aufrufer wird als Windows Dienst ausgeführt. Aufrufer, die nicht als Windows Dienst ausgeführt werden, sollten dieses Flag nicht festlegen. Aufrufer, die als Dienst ausgeführt werden, müssen dieses Flag festlegen.
    
MAPI_NO_COINIT
  
> Legen Sie das flag MAPI_NO_COINT fest, damit **MAPIInitialize** nicht versucht, COM mit einem Aufruf von [CoInitialize zu initialisieren.](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx) Wenn eine **MAPIINIT_0** Struktur an **MAPIInitialize** übergeben wird, wobei  _ulFlags_ auf MAPI_NO_COINIT festgelegt ist, geht MAPI davon aus, dass COM bereits initialisiert wurde, und umgeht den Aufruf von **CoInitialize**.
    
## <a name="remarks"></a>HinwBemerkungeneise

Multithread-Clients sollten das MAPI_MULTITHREAD_NOTIFICATIONS Flag festlegen. Wenn das Flag nicht festgelegt ist, werden Benachrichtigungen in dem Thread generiert, der zum ersten Aufruf von **MAPIInitialize** verwendet wird. 
  
Weitere Informationen dazu, wann Sie dieses Kennzeichen festlegen und wie Sie Threadsicherheit in einem Client implementieren, finden Sie unter [Threading in MAPI.](threading-in-mapi.md) 
  
## <a name="see-also"></a>Siehe auch



[MAPIInitialize](mapiinitialize.md)


[MAPI-Strukturen](mapi-structures.md)

