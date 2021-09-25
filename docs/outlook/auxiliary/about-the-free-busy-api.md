---
title: Informationen zur Frei/Gebucht-API
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Die Frei/Gebucht-API ermöglicht es E-Mail-Anbietern, Frei/Gebucht-Statusinformationen für angegebene Benutzerkonten innerhalb eines bestimmten Zeitraums bereitzustellen.
ms.openlocfilehash: 9b57a2958298098bda119ae260453f56d7cd1fca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580433"
---
# <a name="about-the-freebusy-api"></a>Informationen zur Frei/Gebucht-API

Die Frei/Gebucht-API ermöglicht es E-Mail-Anbietern, Frei/Gebucht-Statusinformationen für angegebene Benutzerkonten innerhalb eines bestimmten Zeitraums bereitzustellen. Der Frei/Gebucht-Status eines Zeitblocks im Kalender eines Benutzers ist einer der folgenden: abwesenheitsfrei, ausgelastet, mit Vorbehalt oder kostenlos.
  
## <a name="create-a-freebusy-provider"></a>Erstellen eines Frei/Gebucht-Anbieters

Um Frei/Gebucht-Informationen für E-Mail-Benutzer bereitzustellen, erstellt ein E-Mail-Anbieter einen Frei/Gebucht-Anbieter und registriert ihn bei Outlook. Der Frei/Gebucht-Anbieter muss die folgenden Schnittstellen implementieren. Beachten Sie, dass eine Reihe von Elementen in diesen Schnittstellen nicht unterstützt wird und die angegebenen Rückgabewerte zurückgeben muss. Insbesondere unterstützt die Frei/Gebucht-API keinen Schreibzugriff auf Frei/Gebucht-Informationen und delegiert den Zugriff auf Konten.
  
- [IFreeBusySupport](ifreebusysupport.md) : Diese Schnittstelle unterstützt die Spezifikation von Schnittstellen, die auf Frei/Gebucht-Daten für angegebene Benutzer zugreifen. Es verwendet [FBUser,](fbuser.md) um einen Benutzer zu identifizieren. 
    
- [IFreeBusyData](ifreebusydata.md) : Diese Schnittstelle ruft einen Zeitraum für einen bestimmten Benutzer ab und legt diesen fest und gibt eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb dieses Zeitraums zurück. Es verwendet relative Zeit, um diesen Zeitraum abzurufen und festzulegen. Weitere Informationen finden Sie unter [Verwenden der relativen Zeit für den Zugriff auf Frei/Gebucht-Daten.](how-to-use-relative-time-to-access-free-busy-data.md)
    
- [IEnumFBBlock](ienumfbblock.md) : Diese Schnittstelle unterstützt den Zugriff auf und das Aufzählen von Frei/Gebucht-Datenblöcken für einen Benutzer innerhalb eines Zeitraums. 
    
   > [!NOTE]
   > Eine Enumeration enthält Frei/Gebucht-Blöcke, die den Frei/Gebucht-Status von Zeiträumen im Kalender eines Benutzers innerhalb eines Zeitraums (angegeben durch [IFreeBusyData::EnumBlocks)](ifreebusydata-enumblocks.md)angeben. Elemente in einem Kalender, z. B. Termine und Besprechungsanfragen, formularblöcke in der Enumeration. Elemente, die im Kalender nebeneinander liegen und den gleichen Frei/Gebucht-Status haben, werden zu einem einzigen Block kombiniert. Ein kostenloser Zeitraum in einem Kalender bildet auch einen Block. Daher hätten keine zwei aufeinander folgenden Blöcke in einer Enumeration den gleichen Frei/Gebucht-Status. Diese Blöcke überlappen sich nicht mit der Zeit. Wenn sich Elemente in einem Kalender überlappen, führt Outlook diese Elemente zu nicht überlappenden Frei/Gebucht-Blöcken in der Enumeration zusammen, basierend auf dieser Rangfolge: außer Haus, beschäftigt, mit Vorbehalt. 
  
Um den Frei/Gebucht-Anbieter bei Outlook zu registrieren, sollte der E-Mail-Anbieter Folgendes tun:
  
1. Registrieren Sie den Frei/Gebucht-Anbieter bei COM, und stellen Sie eine CLSID bereit, die den Zugriff auf die Implementierung von **IFreeBusySupport** durch den Anbieter ermöglicht. 
    
2. Teilen Sie Outlook mit, dass der Frei/Gebucht-Anbieter vorhanden ist, indem Sie den folgenden Schlüssel (wobei `<xx.x>` die Version von Outlook steht) in der Systemregistrierung festlegen: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Wenn der Transportanbieter beispielsweise SMTP ist, legen Sie zum Registrieren des Anbieters bei Microsoft Outlook 2010 den folgenden Schlüssel auf die Daten in der folgenden Tabelle fest: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Name |Typ |Wert |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID für die jeweilige Implementierung von IFreeBusySupport}  |
   
   In diesem Szenario erstellt Outlook die COM-Klasse gemeinsam und verwendet sie, um Frei/Gebucht-Informationen für alle SMTP-E-Mail-Benutzer abzurufen.
    
Um ein Adressbuch und einen Transportanbieter zu unterstützen, die einen anderen Adresseintragstyp als SMTP verwenden, ändern Sie den  *Namen* entsprechend. 
  
> [!NOTE]
> Während der Installation sollten Frei/Gebucht-Anbieter überprüfen, ob bereits eine Registrierungseinstellung für denselben Adresseintragstyp vorhanden ist. Andernfalls sollte der Frei/Gebucht-Anbieter den aktuellen Anbieter für diesen Adresseintragstyp überschreiben und diesen Anbieter wiederherstellen, wenn er deinstalliert wird. Wenn ein Benutzer jedoch mehrere Frei/Gebucht-Anbieter für denselben Adresseintragstyp installiert hat, sollte der Benutzer diese Anbieter in umgekehrter Reihenfolge als Installation deinstallieren (d. b. immer den neuesten Anbieter deinstallieren). Andernfalls verweist die Registrierung möglicherweise auf einen Anbieter, der bereits deinstalliert wurde. 
  
## <a name="api-components"></a>API-Komponenten

Die Frei/Gebucht-API umfasst die folgenden Komponenten:
  
### <a name="definitions"></a>Definitionen

- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Datentypen

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Schnittstellen

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

