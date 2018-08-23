---
title: Verknüpfen mit MAPI-DLL-Dateien
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 428e92dd783368374fa07c8df9629d60e83dd217
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582028"
---
# <a name="linking-to-the-mapi-dlls"></a>Verknüpfen mit MAPI-DLL-Dateien

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI-Clients können mit der MAPI-DLLs implizit oder explizit verknüpfen mithilfe der Windows-Funktionen **LoadLibrary** und **GetProcAddress**. Informationen zum Verknüpfen explizit MAPI-DLLs finden Sie unter [Link zu MAPI-Funktionen](how-to-link-to-mapi-functions.md).
  
MAPI bietet Typ-Definition-Anweisungen in der MAPIX. H-Headerdatei für jede der folgenden Funktionen:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Verwenden Sie diese Typdefinitionen ordnungsgemäß die entsprechenden Einstiegspunkte aufrufen, wenn Sie explizit MAPI-DLLs verknüpfen.
  
Dienstanbieter können nicht-MAPI-Funktionalität enthalten – Features, die nicht vollständig im Zusammenhang mit MAPI sind – in ihre DLL-Datei. Wenn Sie diese Features verwenden müssen, rufen Sie **LoadLibrary** , bevor Sie mit der DLL und **FreeLibrary** nach dessen Verwendung die DLL aus dem Speicher entfernt. Da MAPI-MAPI-Verwendungsmöglichkeiten von einem Dienstanbieter DLL nicht bekannt ist, besteht keine Garantie, dass die DLL bei Bedarf zur Verfügung steht. MAPI wieder einem Dienstanbieter DLL aufgehoben werden nicht mehr von Clients mit aktiver Sitzungen, die die Dienste erfordern. 
  

