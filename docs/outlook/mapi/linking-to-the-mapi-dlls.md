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
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419303"
---
# <a name="linking-to-the-mapi-dlls"></a>Verknüpfen mit MAPI-DLL-Dateien

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Clients können implizit oder explizit mithilfe der Windows **LoadLibrary** und **GetProcAddress** mit den MAPI-DLLs verknüpfen. Informationen zum expliziten Verknüpfen von MAPI-DLLs finden Sie [unter Link zu MAPI-Funktionen](how-to-link-to-mapi-functions.md).
  
MAPI stellt Typdefinitionsanweisungen im MAPIX zur H-Headerdatei für jede der folgenden Funktionen:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Verwenden Sie diese Typdefinitionen, um die entsprechenden Einstiegspunkte korrekt auf aufruft, wenn Sie explizit mit den MAPI-DLLs verknüpfen.
  
Dienstanbieter können Nicht-MAPI-Funktionen – Features, die keinerlei Bezug zu MAPI haben – in ihrer DLL enthalten. Wenn Sie diese Features verwenden müssen, rufen Sie **LoadLibrary** auf, bevor Sie die DLL und **FreeLibrary** verwenden, um die DLL nach der Verwendung aus dem Arbeitsspeicher zu entfernen. Da MAPI keine Nicht-MAPI-Verwendungen einer Dienstanbieter-DLL kennt, gibt es keine Garantie, dass die DLL bei Bedarf verfügbar ist. MAPI gibt eine Dienstanbieter-DLL frei, wenn es keine Clients mehr mit aktiven Sitzungen gibt, die ihre Dienste erfordern. 
  

