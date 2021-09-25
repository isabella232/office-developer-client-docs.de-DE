---
title: Verknüpfen mit MAPI-DLL-Dateien
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 10fa531c8ef11fb14a344957928b20728d39eba7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584178"
---
# <a name="linking-to-the-mapi-dlls"></a>Verknüpfen mit MAPI-DLL-Dateien

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Clients können implizit oder explizit mithilfe der Windows-Funktionen **LoadLibrary** und **GetProcAddress** eine Verknüpfung mit den MAPI-DLLs herstellen. Informationen zum expliziten Verknüpfen von MAPI-DLLs finden Sie unter [Link zu MAPI-Funktionen.](how-to-link-to-mapi-functions.md)
  
MAPI stellt Typdefinitionsanweisungen in MAPIX bereit. H-Headerdatei für jede der folgenden Funktionen:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Verwenden Sie diese Typdefinitionen, um die entsprechenden Einstiegspunkte korrekt aufzurufen, wenn Sie explizit eine Verknüpfung mit den MAPI-DLLs herstellen.
  
Dienstanbieter können Nicht-MAPI-Funktionen – Features, die keine Verbindung mit der MAPI haben – in ihrer DLL enthalten. Wenn Sie diese Features verwenden müssen, rufen Sie **LoadLibrary** auf, bevor Sie die DLL und **FreeLibrary** verwenden, um die DLL nach der Verwendung aus dem Speicher zu entfernen. Da die MAPI keine Nicht-MAPI-Verwendung einer Dienstanbieter-DLL erkennt, gibt es keine Garantie, dass die DLL bei Bedarf verfügbar ist. MAPI gibt eine Dienstanbieter-DLL frei, wenn keine Clients mehr mit aktiven Sitzungen vorhanden sind, die ihre Dienste erfordern. 
  

