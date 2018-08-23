---
title: Informationen über die Replikations-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 272d4147d60df53ef30a668faa8abe89f96cd654
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582322"
---
# <a name="about-the-replication-api"></a>Informationen über die Replikations-API

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Replikation-API bietet die Funktionalität für einen Anbieter für MAPI-Nachricht anmelden zum Synchronisieren von Microsoft Outlook 2013 oder Microsoft Outlook 2010 Elemente zwischen einem Server und einem privaten PST-basierten lokalen Speicher, der für diesen Anbieter erstellt wird. 
  
> [!NOTE]
> Nachricht ein MAPI-Anbieter muss die Replikation API gemäß den Anweisungen in [Über die Replikation Zustandsautomat](about-the-replication-state-machine.md)implementieren. Der Anbieter mithilfe der API nur in einem persönlichen Speicher für sich selbst erstellt haben, und nicht auf persönliche Speicher für andere Anbieter erstellt haben, da persönliche Informationsspeicher für erstellt andere Anbieter möglicherweise bereits eingerichtet haben eigene Replikationsmechanismen mit dem jeweiligen Server. Beispielsweise verwaltet Offlineordnerdatei (OST) eine eigene Replikations-Beziehung mit einem Microsoft Exchange Server. 
  
Um die Replikation-API verwenden, muss ein Anbieter für MAPI-Nachricht Anmelden zuerst öffnen und Text fließt um eine PST-basierten lokalen Speicher durch Aufrufen von **[NSTServiceEntry](nstserviceentry.md)**. Der Anbieter können Sie die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)**, um die Replikation auszuführen. **IPSTX** erfolgt durch Abfragen auf [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), und **IOSTX** durch **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)** angegeben ist. 
  
## <a name="the-iostx-interface"></a>Die IOSTX-Schnittstelle

Die **IOSTX** -Schnittstelle ist die primäre Schnittstelle, die in der Replikation API Synchronisierung ausgeführt wird. **IOSTX** verschiebt den lokalen Speicher durch eine Reihe von Staaten, Abrufen von Informationen zum Änderungen im lokalen Speicher in jedem Status als auch darüber informiert den lokalen Speicher von Änderungen auf dem Server. Die Replikation-API gibt auch viele Datenstrukturen, die die Synchronisierung unterstützen. 
  
Ein Anbieter verwendet als Client für diese API die Replikation-API zur Text fließt um die lokalen Speicher und die Zustände, Navigation, pushen von Änderungen an den Server auf dem lokalen Speicher (beispielsweise Änderungen an der Ordnerhierarchie oder das Hinzufügen neuer Elemente), und das auch abrufen Informationen zu Änderungen auf dem Server und diese Informationen an die **IOSTX** -Schnittstelle bereitstellen. Die Schnittstelle **IOSTX** nimmt inkrementelle Änderung Synchronisierung (ICS) von Microsoft Exchange Server bereitgestellt. Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx). Über **IOSTX**verwendet der Client ICS überwachen und synchronisieren inkrementelle Änderungen an der Hierarchie oder Inhalt in einem lokalen Speicher. 
  
## <a name="the-ipstx-interface"></a>Die IPSTX-Schnittstelle

 **IPSTX** und fünf andere ** IPSTX *n* ** Schnittstellen, die von **IPSTX** erben bieten Hilfsfunktionen, die beim Ausführen einer Replikation über die Schnittstelle **IOSTX** verwendet werden kann. Beispielsweise können **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** Sie mit den lokalen Speicher emulieren von Outlook-Protokoll-Manager, um ausgehende Nachrichten an einen Server Spoolen tätigen. 
  
Weitere Informationen zu Statusübergänge während der Replikation finden Sie unter [Informationen zu der Replikation Zustandsautomat](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>Die API-Replikation

Die Replikation-API bietet die folgenden Definitionen sowie die Datentypen und Schnittstellen. Eine beispielimplementierung von einem Anbieter für umbrochenen Persönliche Ordner-Dateien (PST) finden Sie unter [Über die umbrochen PST -Datei speichern Beispielanbieter](about-the-sample-wrapped-pst-store-provider.md).
  
Definitionen:
  
- [Konstanten für die Replikation API](mapi-constants.md)
    
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
    
- **[SYNCHRONISIERUNGSSTATUS](syncstate.md)**
    
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
    

