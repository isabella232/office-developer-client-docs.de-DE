---
title: Threading in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 15fb6113e9c3428cff3865307736592fd6e2b2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795728"
---
# <a name="threading-in-mapi"></a>Threading in MAPI

  
  
**Betrifft**: Outlook 
  
Ein Thread ist die grundlegende Entität, die ein Betriebssystem CPU-Zeit zuweist. Ein Thread verfügt über eine eigene Register, Stack, Priorität und Speicher, aber eine Adresse Speicherplatz und Verarbeiten von Ressourcen wie Zugriffstoken gemeinsam genutzt. Threads freigeben Arbeitsspeicher, auch mit einem Thread lesen, was ein anderer Thread geschrieben hat.
  
MAPI-Clients verwenden Sie die folgenden generischen threading Modelle.
  
|**Threading-Modell**|**Beschreibung**|
|:-----|:-----|
|Einzelne Threadingmodells  <br/> |Alle Objekte werden in den einzelnen Thread verwendet.  <br/> |
|Des Apartmentthreading Threadingmodells  <br/> |Ein Objekt kann nur in dem Thread verwendet werden, die sie erstellt haben.  <br/> |
|Free-threading, oder der Thread-Modell  <br/> |Ein Objekt kann auf einem beliebigen Thread verwendet werden.  <br/> |
   
MAPI verwendet das kostenlose Threadingmodell unterstützenden threadsicheren Objekten, die auf einem beliebigen Thread können Sie jederzeit verwendet werden können. OLE verwendet die Apartmentthreading-Modells. Das Threadingmodell des Apartmentthreading unterstützt-Objekten, die bei ein Thread als diejenige, die das Objekt erstellt verwenden dieses Objekt muss explizit übertragen werden müssen.
  
Der Mechanismus, den OLE verwendet, um Objekte von einem Thread in eine andere zu übertragen wird als Marshallen bezeichnet. Das Marshallen beinhaltet ein Stubobjekt und ein Proxyobjekt. Diese spezielle Objekte Packen Sie die Parameter der Schnittstelle im Objekt gemarshallt werden, diese Parameter an den anderen Thread übertragen und Entpacken sie nach dem eintreffen. Konflikt zwischen den beiden Multithread-Modellen tritt auf, wenn ein-threading MAPI-Objekt an einen anderen Prozess, die mit OLE "lightweight" Remote Procedure Call oder LRPC gesendet wird. LRPC Semantik des Objekts von free-threading zu Apartmentthreading durch interposing Stub und des Proxys Schnittstellen mit Apartmentthreading-Verhalten zwischen dem Objekt und seine Aufrufer geändert. Zur Förderung des Bekanntheitsgrads der Situationen in MAPI, die zu dieser Konflikt führen kann Clients und Dienstanbieter können Probleme.
  
Ein MAPI-Objekt kann zugegriffen werden:
  
- Über direkte Aufrufe von dessen eine Schnittstelle mit Methoden verknüpft von einem Dienstanbieter oder MAPI zurückgegebene Zeiger an den Client-Prozess wie das Sitzungsobjekt von [MAPILogonEx](mapilogonex.md)zurückgegeben.
    
- Unter Verwendung eines Schnittstelle Zeigers zurückgegeben, die für alle Dienstanbieter, wie etwa das Folder-Objekt kopiert über indirekte Aufrufe der Methoden aus einem anderen Ordner im [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)haben.
    
- Über eine Callback-Funktion wie die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode übergebenen mit einem Dienstanbieter oder MAPI einen **Advise** -Anruf oder die Methoden, die auf einer langen Operation Fortschritt anzeigen können. 
    

