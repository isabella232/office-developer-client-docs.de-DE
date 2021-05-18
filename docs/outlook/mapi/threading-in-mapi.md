---
title: Threading in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405541"
---
# <a name="threading-in-mapi"></a>Threading in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Thread ist die grundlegende Entität, der ein Betriebssystem CPU-Zeit zurteilung. Ein Thread verfügt über eigene Register, Stapel, Priorität und Speicher, teilt sich jedoch einen Adressraum und Prozessressourcen wie Zugriffstoken. Threads teilen auch Arbeitsspeicher, und ein Thread liest, was ein anderer Thread geschrieben hat.
  
MAPI-Clients verwenden die folgenden generischen Threadingmodelle.
  
|**Threadmodell**|**Beschreibung**|
|:-----|:-----|
|Einzelnes Threadmodell  <br/> |Alle Objekte werden im einzelnen Thread verwendet.  <br/> |
|Apartmentthreadingmodell  <br/> |Ein Objekt kann nur für den Thread verwendet werden, von dem es erstellt wurde.  <br/> |
|Kostenloses Threading oder Threadpartmodell  <br/> |Ein Objekt kann für jeden Thread verwendet werden.  <br/> |
   
MAPI verwendet das kostenlose Threadingmodell, das threadsichere Objekte unterstützt, die jederzeit in jedem Thread verwendet werden können. OLE verwendet das Apartmentthreadmodell. Das Apartmentthreadmodell unterstützt Objekte, die explizit übertragen werden müssen, wenn ein anderer Thread als der, der das Objekt erstellt hat, dieses Objekt verwenden muss.
  
Der Mechanismus, den OLE zum Übertragen von Objekten von einem Thread in einen anderen verwendet, wird als Marshalling bezeichnet. Das Marshalling umfasst ein Stubobjekt und ein Proxyobjekt. Diese speziellen Objekte verpacken die Parameter der Schnittstelle im Zu marshallenden Objekt, übertragen diese Parameter an den anderen Thread und packen sie bei der Ankunft aus. Konflikt zwischen den beiden Multithreadmodellen tritt auf, wenn ein freithreading-MAPI-Objekt mithilfe von OLE "lightweight" Remote Procedure Call oder EINEMFN an einen anderen Prozess gesendet wird. DURCH DIE ARBEIT WIRD die Semantik des Objekts vom freien Threading zum Apartmentthreading geändert, indem Stub- und Proxyschnittstellen mit dem Verhalten des Apartmentthreads zwischen dem Objekt und dem Aufrufer interposiert werden. Das Bewusstsein für die Situationen in MAPI, die zu diesem Konflikt führen, kann Clients und Dienstanbietern helfen, Probleme zu verhindern.
  
Auf ein MAPI-Objekt kann zugegriffen werden:
  
- Durch direkte Aufrufe seiner Methoden mithilfe eines Schnittstellenzeigers, der von einem Dienstanbieter oder mapI zurückgegeben wird, der mit dem Clientprozess verknüpft ist, z. B. das sitzungsobjekt, das von [MAPILogonEx](mapilogonex.md)zurückgegeben wird.
    
- Durch indirekte Aufrufe seiner Methoden mithilfe eines von einem beliebigen Dienstanbieter zurückgegebenen Schnittstellenzeigers, z. B. des ordnerobjekts, das aus einem anderen Ordner in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)kopiert wurde.
    
- Über eine Rückruffunktion, z. B. die [ANAPIAdviseSink::OnNotify-Methode,](imapiadvisesink-onnotify.md) die an einen Dienstanbieter oder mapI in einem **Advise-Aufruf** übergeben wird, oder die Methoden, die den Fortschritt eines langwierigen Vorgangs anzeigen können. 
    

