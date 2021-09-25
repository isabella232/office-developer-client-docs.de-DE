---
title: Threading in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 40b313b979a8fafab5fca72b23bfdbc4dd65c86d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566276"
---
# <a name="threading-in-mapi"></a>Threading in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Thread ist die grundlegende Entität, der ein Betriebssystem CPU-Zeit zuweist. Ein Thread verfügt über eigene Register, Stapel, Priorität und Speicher, teilt jedoch einen Adressraum und Prozessressourcen wie Zugriffstoken. Threads teilen auch Arbeitsspeicher, wobei ein Thread liest, was ein anderer Thread geschrieben hat.
  
MAPI-Clients verwenden die folgenden generischen Threadingmodelle.
  
|**Threadingmodell**|**Beschreibung**|
|:-----|:-----|
|SingleThreading-Modell  <br/> |Alle Objekte werden im einzelnen Thread verwendet.  <br/> |
|Apartmentthreadingmodell  <br/> |Ein Objekt kann nur in dem Thread verwendet werden, der es erstellt hat.  <br/> |
|Kostenloses Threading oder Thread-Party-Modell  <br/> |Ein Objekt kann in jedem Thread verwendet werden.  <br/> |
   
MAPI verwendet das Freithreadingmodell und unterstützt threadsichere Objekte, die jederzeit in jedem Thread verwendet werden können. OLE verwendet das Apartmentthreadingmodell. Das Apartmentthreadingmodell unterstützt Objekte, die explizit übertragen werden müssen, wenn ein anderer Thread als der, der das Objekt erstellt hat, dieses Objekt verwenden muss.
  
Der Mechanismus, mit dem OLE Objekte von einem Thread in einen anderen überträgt, wird als Marshalling bezeichnet. Das Marshalling umfasst ein Stubobjekt und ein Proxyobjekt. Diese speziellen Objekte packen die Parameter der Schnittstelle im zu marshallenden Objekt, übertragen diese Parameter in den anderen Thread und entpacken sie beim Eintreffen. Ein Konflikt zwischen den beiden Multithreadmodellen entsteht, wenn ein MAPI-Objekt mit freiem Threading an einen anderen Prozess mithilfe des OLE-"lightweight"-Remoteprozeduraufrufs oder LRPC gesendet wird. LRPC ändert die Semantik des Objekts von Freithreading zu Apartmentthreading, indem Stub- und Proxyschnittstellen mit Apartmentthreadingverhalten zwischen dem Objekt und dessen Aufrufer interposiert werden. Das Bewusstsein für die Situationen in der MAPI, die zu diesem Konflikt führen, kann Clients und Dienstanbietern dabei helfen, Probleme zu verhindern.
  
Auf ein MAPI-Objekt kann zugegriffen werden:
  
- Durch direkte Aufrufe seiner Methoden mithilfe eines Schnittstellenzeigers, der von einem Dienstanbieter oder einer MAPI zurückgegeben wird, die mit dem Prozess des Clients verknüpft ist, z. B. das von [MAPILogonEx](mapilogonex.md)zurückgegebene Sitzungsobjekt.
    
- Durch indirekte Aufrufe seiner Methoden mithilfe eines Schnittstellenzeigers, der von einem beliebigen Dienstanbieter zurückgegeben wird, z. B. das Ordnerobjekt, das aus einem anderen Ordner in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)kopiert wurde.
    
- Über eine Rückruffunktion, z. B. die [IMAPIAdviseSink::OnNotify-Methode,](imapiadvisesink-onnotify.md) die an einen Dienstanbieter oder an die MAPI in einem **Advise-Aufruf** übergeben wird, oder über die Methoden, die den Fortschritt eines längeren Vorgangs anzeigen können. 
    

