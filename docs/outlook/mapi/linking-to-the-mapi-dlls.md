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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270042"
---
# <a name="linking-to-the-mapi-dlls"></a>Verknüpfen mit MAPI-DLL-Dateien

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Clients können implizit oder explizit mithilfe der Windows-Funktionen **LoadLibrary** und **GetProcAddress**eine Verknüpfung zu den MAPI-DLLs herstellen. Informationen zum expliziten Verknüpfen von MAPI-DLLs finden Sie unter [Link to MAPI Functions](how-to-link-to-mapi-functions.md).
  
MAPI stellt typdefinitions Anweisungen in der MAPIX bereit. H-Headerdatei für jede der folgenden Funktionen:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Verwenden Sie diese Typdefinitionen, um die entsprechenden Einstiegspunkte richtig aufzurufen, wenn Sie explizit mit den MAPI-DLLs verknüpfen.
  
Dienstanbieter können nicht-MAPI-Funktionen enthalten, die vollständig mit MAPI in Verbindung stehen (in Ihrer DLL). Wenn Sie diese Funktionen verwenden müssen, rufen Sie **LoadLibrary** vor der Verwendung der dll und **FreeLibrary** , um die dll aus dem Speicher nach ihrer Verwendung zu entfernen. Da MAPI die nicht-MAPI-Verwendung einer Dienstanbieter-DLL nicht kennt, gibt es keine Garantie dafür, dass die DLL bei Bedarf verfügbar ist. MAPI gibt eine Dienstanbieter-DLL frei, wenn es keine Clients mit aktiven Sitzungen mehr gibt, die deren Dienste erfordern. 
  

