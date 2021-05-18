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
  
Die Replikations-API bietet die Funktionalität für einen MAPI-Nachrichtenspeicheranbieter zum Synchronisieren von Microsoft Outlook 2013- oder Microsoft Outlook 2010-Elementen zwischen einem Server und einem privaten lokalen PST-basierten Speicher, der für diesen Anbieter erstellt wird. 
  
> [!NOTE]
> Ein MAPI-Nachrichtenspeicheranbieter muss die Replikations-API gemäß den Anweisungen unter [Informationen zum Replikationsstatuscomputer implementieren.](about-the-replication-state-machine.md) Der Anbieter darf die API nur für einen persönlichen Speicher verwenden, der für sich selbst erstellt wurde, und nicht für persönliche Speicher, die für andere Anbieter erstellt wurden, da persönliche Speicher, die für andere Anbieter erstellt wurden, möglicherweise bereits eigene Replikationsmechanismen mit dem jeweiligen Server eingerichtet haben. Beispielsweise pflegt eine Offlineordnerdatei (OST) eine eigene Replikationsbeziehung mit einem Microsoft Exchange Server. 
  
Um die Replikations-API zu verwenden, muss ein MAPI-Nachrichtenspeicheranbieter zunächst einen PST-basierten lokalen Speicher öffnen und umschließen, indem **[er NSTServiceEntry aufruft.](nstserviceentry.md)** Der Anbieter kann dann die Hauptschnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation zu durchführen. **IPSTX wird** durch Abfragen auf [IMsgStore bereitgestellt: IMAPIProp](imsgstoreimapiprop.md)und **IOSTX** wird von **[IPSTX::GetSyncObject bereitgestellt.](ipstx-getsyncobject.md)** 
  
## <a name="the-iostx-interface"></a>Die IOSTX-Schnittstelle

Die **IOSTX-Schnittstelle** ist die primäre Schnittstelle, die die Synchronisierung in der Replikations-API durchführt. **IOSTX** verschiebt den lokalen Speicher durch eine Reihe von Zustände, ruft Informationen in jedem Status zu Änderungen im lokalen Speicher ab und informiert den lokalen Speicher über Änderungen auf dem Server. Die Replikations-API gibt außerdem viele Datenstrukturen an, die die Synchronisierung unterstützen. 
  
Ein Speicheranbieter verwendet als Client für diese API die Replikations-API, um den lokalen Speicher zu umschließen und diese Zustände zu durchziehen, Änderungen am lokalen Speicher (z. B. Änderungen an der Ordnerhierarchie oder das Hinzufügen neuer Elemente) auf den Server zu verschieben und informationen zu Änderungen auf dem Server zu erhalten und diese Informationen an die **IOSTX-Schnittstelle zu** senden. Die **IOSTX-Schnittstelle** übernimmt die inkrementelle Änderungssynchronisierung (Incremental Change Synchronization, ICS), die von Microsoft Exchange Server. Weitere Informationen zu ICS finden Sie unter [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx). Über **IOSTX** verwendet der Client ICS, um inkrementelle Änderungen an der Hierarchie oder den Inhalten in einem lokalen Speicher zu überwachen und zu synchronisieren. 
  
## <a name="the-ipstx-interface"></a>Die IPSTX-Schnittstelle

 **IPSTX** und fünf weitere **IPSTX n ** -Schnittstellen, die von **IPSTX** *erben,* bieten Hilfsfunktionen, die bei der Replikation über die **IOSTX-Schnittstelle verwendet werden** können. Mit **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** können Sie beispielsweise den Outlook-Protokoll-Manager emulieren lassen, um ausgehende Nachrichten an einen Server zu spoolen. 
  
Weitere Informationen zu Statusübergängen während der Replikation finden Sie [unter Informationen zum Replikationsstatuscomputer](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>Die Replikations-API

Die Replikations-API bietet die folgenden Defintions, Datentypen und Schnittstellen. Eine Beispielimplementierung eines Speicheranbieters für umschlossene Persönliche Ordnerdateien (PST) finden Sie unter [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).
  
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
    

