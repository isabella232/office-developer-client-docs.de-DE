---
title: Informationen über die Replikations-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 1d0d67c9a766ebafec6d44e3e54986f50bf7b4d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592741"
---
# <a name="about-the-replication-api"></a>Informationen über die Replikations-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Replikations-API stellt die Funktionalität für einen MAPI-Nachrichtenspeicheranbieter bereit, um Microsoft Outlook 2013 oder Microsoft Outlook 2010 Elemente zwischen einem Server und einem privaten PST-basierten lokalen Speicher zu synchronisieren, der für diesen Anbieter erstellt wird. 
  
> [!NOTE]
> Ein MAPI-Nachrichtenspeicheranbieter muss die Replikations-API gemäß den Anweisungen unter ["Informationen zum Replikationsstatuscomputer"](about-the-replication-state-machine.md)implementieren. Der Anbieter darf die API nur für einen persönlichen Speicher verwenden, der für sich selbst erstellt wurde, und nicht für persönliche Speicher, die für andere Anbieter erstellt wurden, da persönliche Speicher, die für andere Anbieter erstellt wurden, möglicherweise bereits eigene Replikationsmechanismen mit dem entsprechenden Server eingerichtet haben. Beispielsweise behält eine Offlineordnerdatei (OST) eine eigene Replikationsbeziehung mit einem Microsoft Exchange-Server bei. 
  
Um die Replikations-API zu verwenden, muss ein MAPI-Nachrichtenspeicheranbieter zuerst einen PST-basierten lokalen Speicher öffnen und umschließen, indem **[er NSTServiceEntry aufruft.](nstserviceentry.md)** Der Anbieter kann dann die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX,](ipstxiunknown.md)** verwenden, um die Replikation durchzuführen. **IPSTX** wird durch Abfragen in [IMsgStore bereitgestellt: IMAPIProp,](imsgstoreimapiprop.md)und **IOSTX** wird von **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)** bereitgestellt. 
  
## <a name="the-iostx-interface"></a>Die IOSTX-Schnittstelle

Die **IOSTX-Schnittstelle** ist die primäre Schnittstelle, die eine Synchronisierung in der Replikations-API durchführt. **IOSTX** verschiebt den lokalen Speicher durch eine Reihe von Zuständen, wobei Informationen in jedem Zustand zu Änderungen im lokalen Speicher abgerufen und der lokale Speicher über Änderungen auf dem Server informiert wird. Die Replikations-API gibt auch viele Datenstrukturen an, die die Synchronisierung unterstützen. 
  
Ein Speicheranbieter verwendet als Client für diese API die Replikations-API, um den lokalen Speicher zu umschließen und durch diese Zustände zu navigieren, Änderungen an den lokalen Speicher (z. B. Änderungen an der Ordnerhierarchie oder das Hinzufügen neuer Elemente) an den Server weiterzuleiten sowie Informationen zu Änderungen auf dem Server abzurufen und diese Informationen an die **IOSTX-Schnittstelle** bereitzustellen. Die **IOSTX-Schnittstelle** übernimmt die inkrementelle Änderungssynchronisierung (Incremental Change Synchronization, ICS), die von Microsoft Exchange Server bereitgestellt wird. Weitere Informationen zu ICS finden Sie unter [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx). Über **IOSTX** verwendet der Client ICS, um inkrementelle Änderungen an der Hierarchie oder dem Inhalt in einem lokalen Speicher zu überwachen und zu synchronisieren. 
  
## <a name="the-ipstx-interface"></a>Die IPSTX-Schnittstelle

 **IPSTX** und fünf weitere **IPSTX n **-Schnittstellen, die von **IPSTX** *erben,* bieten Hilfsfunktionen, die bei der Replikation über die **IOSTX-Schnittstelle** verwendet werden können. Beispielsweise können Sie mit **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** festlegen, dass der lokale Speicher den Outlook Protokoll-Manager emuliert, um ausgehende Nachrichten an einen Server zu senden. 
  
Weitere Informationen zu Statusübergängen während der Replikation finden Sie unter [Informationen zum Replikationsstatuscomputer.](about-the-replication-state-machine.md)
  
## <a name="the-replication-api"></a>Die Replikations-API

Die Replikations-API bietet die folgenden Definitionen, Datentypen und Schnittstellen. Eine Beispielimplementierung eines Speicheranbieters für umschlossene Persönliche Ordner-Dateien (PST) finden Sie unter ["Beispiel für umschlossene PST-Store Anbieter".](about-the-sample-wrapped-pst-store-provider.md)
  
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
    

