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
  
Ein Thread ist die grundlegende Entität, in die ein Betriebssystem CPU-Zeit zuordnet. Ein Thread verfügt über eigene Register, Stapel, Priorität und Speicher, hat jedoch einen Adressraum und verarbeitet Ressourcen wie Zugriffstoken. Threads teilen auch Arbeitsspeicher, wobei ein Thread liest, was ein anderer Thread geschrieben hat.
  
MAPI-Clients verwenden die folgenden generischen Threadingmodelle.
  
|**Threadingmodell**|**Beschreibung**|
|:-----|:-----|
|Single Threading-Modell  <br/> |Alle Objekte werden im einzelnen Thread verwendet.  <br/> |
|Apartment-Threading-Modell  <br/> |Ein Objekt kann nur für den Thread verwendet werden, der es erstellt hat.  <br/> |
|Freies Threading oder Thread-Party-Modell  <br/> |Ein Objekt kann in einem beliebigen Thread verwendet werden.  <br/> |
   
MAPI verwendet das ﻿kostenlose Threadingmodell und unterstützt threadsichere Objekte, die jederzeit in einem beliebigen Thread verwendet werden können. OLE verwendet das Apartment-Threadingmodell. Das Apartment-Threading-Modell unterstützt Objekte, die explizit übergeben werden müssen, wenn ein anderer Thread als derjenige, der das Objekt erstellt hat, dieses Objekt verwenden muss.
  
Der Mechanismus, den OLE zum Übertragen von Objekten von einem Thread zu einem anderen verwendet, wird als Marshalling bezeichnet. Marshalling umfasst ein Stub-Objekt und ein Proxy-Objekt. Diese speziellen Objekte verpacken die Parameter der Schnittstelle im Objekt, das gemarshallt werden soll, übertragen diese Parameter in den anderen Thread und entpacken Sie bei der Ankunft. Der Konflikt zwischen den beiden Multithread-Modellen ergibt sich, wenn ein MAPI-Objekt mit freiem Threading an einen anderen Prozess mithilfe von OLE "Lightweight"-Remote Prozeduraufruf oder LRPC gesendet wird. LRPC ändert die Semantik des Objekts vom freien Threading in den Apartmentthreading, indem Stub-und Proxy Schnittstellen mit dem Apartmentthreading-Verhalten zwischen dem Objekt und seinem Aufrufer zwischen den Objekten ausgerichtet werden. Das Bewusstsein für die Situationen in MAPI, die zu diesem Konflikt führen, kann dazu beitragen, dass Clients und Dienstanbieter Probleme vermeiden.
  
Auf ein MAPI-Objekt kann zugegriffen werden:
  
- Durch direkte Aufrufe seiner Methoden mithilfe eines Schnittstellenzeigers, der von einem Dienstanbieter oder einer mit dem Prozess des Clients verknüpften MAPI zurückgegeben wird, wie beispielsweise das von [MAPILogonEx](mapilogonex.md)zurückgegebene Sitzungsobjekt.
    
- Durch indirekte Aufrufe seiner Methoden mithilfe eines von einem beliebigen Dienstanbieter zurückgegebenen Schnittstellenzeigers, wie beispielsweise des Folder-Objekts, das aus einem anderen Ordner in [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md)kopiert wurde.
    
- Über eine Rückruffunktion, wie beispielsweise die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode, die an einen Dienstanbieter oder an MAPI in einem **Advise** -Aufruf übergeben wird, oder die Methoden, die den Fortschritt bei einem langwierigen Vorgang anzeigen können. 
    

