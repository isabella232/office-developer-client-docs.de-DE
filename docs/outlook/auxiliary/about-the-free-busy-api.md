---
title: Informationen zur Frei/Gebucht-API
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Die Frei/Gebucht-API ermöglicht E-Mail-Anbietern, Frei/Gebucht-Statusinformationen für angegebene Benutzerkonten innerhalb eines angegebenen Zeitbereichs zur Verfügung zu stellen.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433759"
---
# <a name="about-the-freebusy-api"></a>Informationen zur Frei/Gebucht-API

Die Frei/Gebucht-API ermöglicht E-Mail-Anbietern, Frei/Gebucht-Statusinformationen für angegebene Benutzerkonten innerhalb eines angegebenen Zeitbereichs zur Verfügung zu stellen. Der Frei/Gebucht-Status eines Zeitblocks im Kalender eines Benutzers ist einer der folgenden: out-of-office, busy, tentative oder free.
  
## <a name="create-a-freebusy-provider"></a>Erstellen eines Frei/Gebucht-Anbieters

Um E-Mail-Benutzern Frei/Gebucht-Informationen zur Verfügung zu stellen, erstellt ein E-Mail-Anbieter einen Frei/Gebucht-Anbieter und registriert Outlook. Der Frei/Gebucht-Anbieter muss die folgenden Schnittstellen implementieren. Beachten Sie, dass eine Reihe von Mitgliedern in diesen Schnittstellen nicht unterstützt wird und die angegebenen Rückgabewerte zurückgeben müssen. Insbesondere unterstützt die Frei/Gebucht-API keinen Schreibzugriff auf Frei/Gebucht-Informationen und delegiert den Zugriff auf Konten.
  
- [IFreeBusySupport](ifreebusysupport.md) – Diese Schnittstelle unterstützt die Spezifikation von Schnittstellen, die auf Frei/Gebucht-Daten für bestimmte Benutzer zugreifen. Es verwendet [FBUser,](fbuser.md) um einen Benutzer zu identifizieren. 
    
- [IFreeBusyData](ifreebusydata.md) – Diese Schnittstelle ruft einen Zeitraum für einen bestimmten Benutzer ab und legt diesen fest und gibt eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb dieses Zeitbereichs zurück. Es verwendet relative Zeit, um diesen Zeitraum zu erhalten und zu legen. Weitere Informationen finden Sie unter [Verwenden der relativen Zeit für den Zugriff auf Frei/Gebucht-Daten.](how-to-use-relative-time-to-access-free-busy-data.md)
    
- [IEnumFBBlock](ienumfbblock.md) – Diese Schnittstelle unterstützt den Zugriff auf und das Aufzählen von Frei/Gebucht-Datenblöcken für einen Benutzer innerhalb eines Zeitbereichs. 
    
   > [!NOTE]
   > Eine Enumeration enthält Frei/Gebucht-Blöcke, die den Frei/Gebucht-Status von Zeiträumen im Kalender eines Benutzers innerhalb eines Zeitbereichs angeben (angegeben durch [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)). Elemente in einem Kalender, z. B. Termine und Besprechungsanfragen, Formularblöcke in der Enumeration. Elemente, die im Kalender nebeneinander liegen und den gleichen Frei/Gebucht-Status haben, werden zu einem einzelnen Block kombiniert. Ein kostenloser Zeitraum in einem Kalender bildet auch einen Block. Daher hätten keine zwei aufeinander folgenden Blöcke in einer Enumeration den gleichen Frei/Gebucht-Status. Diese Blöcke überlappen sich nicht in der Zeit. Wenn in einem Kalender überlappende Elemente enthalten sind, führt Outlook diese Elemente zu nicht überlappenden Frei/Gebucht-Blöcken in der Enumeration basierend auf dieser Rangfolge zusammen: out-of-office, busy, tentative. 
  
Um den Frei/Gebucht-Anbieter bei Outlook registrieren zu können, sollte der E-Mail-Anbieter die folgenden Schritte tun:
  
1. Registrieren Sie den Frei/Gebucht-Anbieter bei COM, indem Sie eine CLSID bereitstellen, die den Zugriff auf die Implementierung von **IFreeBusySupport durch den Anbieter ermöglicht.** 
    
2. Teilen Outlook, dass der Frei/Gebucht-Anbieter vorhanden ist, indem Sie den folgenden Schlüssel (wobei die Version von Outlook) in der `<xx.x>` Systemregistrierung festlegen: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Wenn der Transportanbieter beispielsweise SMTP ist, legen Sie den folgenden Schlüssel auf die Daten in der folgenden Tabelle, um den Anbieter bei Microsoft Outlook 2010 zu registrieren: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Name |Typ |Wert |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID für die jeweilige Implementierung von IFreeBusySupport}  |
   
   In diesem Szenario erstellt Outlook die COM-Klasse und verwendet sie zum Abrufen von Frei/Gebucht-Informationen für smtp-E-Mail-Benutzer.
    
Um ein Adressbuch und einen Transportanbieter zu unterstützen, die einen anderen Adresseintragstyp als SMTP verwenden, ändern Sie den  *Namen* entsprechend. 
  
> [!NOTE]
> Während der Installation sollten Frei/Gebucht-Anbieter überprüfen, ob bereits eine Registrierungseinstellung für denselben Adresseintragstyp vorhanden ist. In diesem Zustand sollte der Frei/Gebucht-Anbieter den aktuellen Anbieter für diesen Adresseintragstyp überschreiben und bei der Deinstallation in diesem Anbieter wiederherstellen. Wenn ein Benutzer jedoch mehrere Frei/Gebucht-Anbieter für denselben Adresseintragstyp installiert hat, sollte der Benutzer diese Anbieter in umgekehrter Reihenfolge als Installation deinstallieren (d. h. immer den neuesten Anbieter deinstallieren). Andernfalls kann die Registrierung auf einen Anbieter verweisen, der bereits deinstalliert wurde. 
  
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
    

