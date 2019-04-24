---
title: Informationen über die Replikations-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329519"
---
# <a name="about-the-replication-api"></a>Informationen über die Replikations-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Replikations-API bietet die Funktionalität für einen MAPI-Nachrichtenspeicher Anbieter zum Synchronisieren von Microsoft Outlook 2013-oder Microsoft Outlook 2010-Elementen zwischen einem Server und einem privaten PST-basierten lokalen Speicher, der für diesen Anbieter erstellt wird. 
  
> [!NOTE]
> Ein MAPI-Nachrichtenspeicher Anbieter muss die Replikations-API gemäß den Anweisungen in [über den Replikationsstatus Computer](about-the-replication-state-machine.md)implementieren. Der Anbieter muss die API nur in einem persönlichen Informationsspeicher verwenden, der für sich selbst erstellt wurde, und nicht in persönlichen speichern, die für andere Anbieter erstellt wurden, da persönliche Speicher, die für andere Anbieter erstellt wurden, möglicherweise bereits eigene Replikationsmechanismen mit dem jeweiligen Server eingerichtet haben. Beispielsweise pflegt eine Offlineordnerdatei (Ost) eine eigene Replikationsbeziehung mit einem Microsoft Exchange-Server. 
  
Um die Replikations-API verwenden zu können, muss ein MAPI-Nachrichtenspeicher Anbieter zunächst einen PST-basierten lokalen Speicher öffnen und einbinden, indem er **[NSTServiceEntry](nstserviceentry.md)** aufruft. Der Anbieter kann dann die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation durchzuführen. **IPSTX** wird durch Abfragen in [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)und **IOSTX** von **[IPSTX::](ipstx-getsyncobject.md)** getsyncobject bereitgestellt. 
  
## <a name="the-iostx-interface"></a>Die IOSTX-Schnittstelle

Die **IOSTX** -Schnittstelle ist die primäre Schnittstelle, die die Synchronisierung in der Replikations-API ausführt. **IOSTX** verschiebt den lokalen Speicher über eine Reihe von Zuständen, ruft Informationen in jedem Status zu Änderungen im lokalen Speicher ab und informiert den lokalen Speicher über Änderungen auf dem Server. Die Replikations-API gibt außerdem viele Datenstrukturen an, die die Synchronisierung unterstützen. 
  
Ein Speicheranbieter als Client für diese API verwendet die Replikations-API zum Umschließen des lokalen Speichers und zum Durchlaufen dieser Zustände, wodurch Änderungen im lokalen Speicher (beispielsweise Änderungen an der Ordnerhierarchie oder das Hinzufügen neuer Elemente) zum Server und zum Abrufen von Informationen zu Änderungen auf dem Server und zur bereitstellungdieser Informationen für die **IOSTX** -Schnittstelle. Die **IOSTX** -Schnittstelle übernimmt die von Microsoft Exchange Server bereitgestellte inkrementelle Änderungs Synchronisierung (ICS). Weitere Informationen zu ICS finden Sie unter [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx). Über **IOSTX**verwendet der Client ICS zum Überwachen und Synchronisieren von inkrementellen Änderungen an der Hierarchie oder den Inhalten in einem lokalen Speicher. 
  
## <a name="the-ipstx-interface"></a>Die IPSTX-Schnittstelle

 **IPSTX** und fünf weitere * * IPSTX *n* * *-Schnittstellen, die von **IPSTX** erben, bieten Hilfsfunktionen, die beim Durchführen der Replikation über die **IOSTX** -Schnittstelle verwendet werden können. Beispielsweise ermöglicht **[IPSTX:: EmulateSpooler](ipstx-emulatespooler.md)** , dass der lokale Speicher den Outlook-Protokoll-Manager emuliert, um ausgehende Nachrichten an einen Server zu spoolen. 
  
Weitere Informationen über Statusübergänge während der Replikation finden Sie unter Informationen zum [Replikationsstatus Computer](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>Die Replikations-API

Die Replikations-API bietet die folgenden Definitionen, Datentypen und Schnittstellen. Eine Beispielimplementierung eines Speicheranbieters für eingebundene persönliche Ordner-Dateien (PST) finden Sie unter Informationen zum einGebundenen [PST-Speicheranbieter](about-the-sample-wrapped-pst-store-provider.md).
  
Definitionen:
  
- [Konstanten für die Replikations-API](mapi-constants.md)
    
Funktionen:
  
- **[NSTServiceEntry](nstserviceentry.md)**
    
Datentypen:
  
- **[DNHIER](dnhier.md)**
    
- **[DNTBL](dntbl.md)**
    
- **[DNTBLE](dntble.md)**
    
- **[FEID](feid.md)**
    
- **[HDRSYNC](hdrsync.md)**
    
- **[LTID](ltid.md)**
    
- **[MEID](meid.md)**
    
- **[OLFI](olfi.md)**
    
- **[SKEY](skey.md)**
    
- **[SYNC](sync.md)**
    
- **[SYNCCONT](synccont.md)**
    
- **[SYNCSTATE](syncstate.md)**
    
- **[UPDEL](updel.md)**
    
- **[UPDELE](updele.md)**
    
- **[UPFLD](upfld.md)**
    
- **[UPHIER](uphier.md)**
    
- **[UPMOV](upmov.md)**
    
- **[UPMSG](upmsg.md)**
    
- **[UPREAD](upread.md)**
    
- **[UPREADE](upreade.md)**
    
- **[UPTBL](uptbl.md)**
    
- **[UPTBLE](uptble.md)**
    
Schnittstellen:
  
- **[IOSTX](iostxiunknown.md)**
    
- **[IPSTX](ipstxiunknown.md)**
    
- **[IPSTX2](ipstx2ipstx.md)**
    
- **[IPSTX3](ipstx3ipstx2.md)**
    
- **[IPSTX4](ipstx4ipstx3.md)**
    
- **[IPSTX5](ipstx5ipstx4.md)**
    
- **[IPSTX6](ipstx6ipstx5.md)**
    

