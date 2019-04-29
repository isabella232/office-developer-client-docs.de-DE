---
title: Informationen zur Frei/Gebucht-API
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Die Frei/Gebucht-API ermöglicht es e-Mail-Anbietern, frei/gebucht-Statusinformationen für bestimmte Benutzerkonten innerhalb eines angegebenen Zeitintervalls bereitzustellen.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433759"
---
# <a name="about-the-freebusy-api"></a>Informationen zur Frei/Gebucht-API

Die Frei/Gebucht-API ermöglicht es e-Mail-Anbietern, frei/gebucht-Statusinformationen für bestimmte Benutzerkonten innerhalb eines angegebenen Zeitintervalls bereitzustellen. Der Frei/Gebucht-Status eines Zeitblocks im Kalender eines Benutzers ist einer der folgenden: Abwesenheit, beschäftigt, mit Vorbehalt oder kostenlos.
  
## <a name="create-a-freebusy-provider"></a>Erstellen eines frei/gebucht-Anbieters

Um e-Mail-Benutzern frei/Gebucht-Informationen bereitzustellen, erstellt ein e-Mail-Anbieter einen frei/gebucht-Anbieter und registriert ihn in Outlook. Der frei/gebucht-Anbieter muss die folgenden Schnittstellen implementieren. Beachten Sie, dass eine Reihe von Elementen in diesen Schnittstellen nicht unterstützt wird und die angegebenen Rückgabewerte zurückgegeben werden muss. Insbesondere unterstützt die Frei/Gebucht-API keinen Schreibzugriff auf Frei/Gebucht-Informationen und delegieren den Zugriff auf Konten.
  
- [IFreeBusySupport](ifreebusysupport.md) : Diese Schnittstelle unterstützt die Spezifikation von Schnittstellen, die auf Frei/Gebucht-Daten für bestimmte Benutzer zugreifen. Es verwendet [FBUser](fbuser.md) , um einen Benutzer zu identifizieren. 
    
- [IFreeBusyData](ifreebusydata.md) – diese Schnittstelle Ruft einen Zeitbereich für einen bestimmten Benutzer ab und legt ihn fest und gibt eine Schnittstelle zum Auflisten von Frei/Gebucht-Datenblöcken innerhalb dieses Zeitintervalls zurück. Es verwendet relative Zeit zum Abrufen und Festlegen dieses Zeitintervalls. Weitere Informationen finden Sie unter [Verwenden von relativer Zeit für den Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md).
    
- [IEnumFBBlock](ienumfbblock.md) : Diese Schnittstelle unterstützt den Zugriff auf und das Aufzählen von Frei/Gebucht-Datenblöcken für einen Benutzer innerhalb eines Zeitintervalls. 
    
   > [!NOTE]
   > Eine Aufzählung enthält frei/gebucht-Blöcke, die den Frei/Gebucht-Status von Zeiträumen im Kalender eines Benutzers innerhalb eines Zeitintervalls angeben (angegeben durch [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md)). Elemente in einem Kalender, wie Termine und Besprechungsanfragen, Formular Blöcke in der Aufzählung. Elemente, die sich nebeneinander im Kalender befinden und den gleichen Frei/Gebucht-Status aufweisen, werden zu einem einzigen Block kombiniert. Ein freier Zeitraum in einem Kalender bildet auch einen Block. Daher hätten keine zwei aufeinanderfolgenden Blöcke in einer Enumeration denselben Frei/Gebucht-Status. Diese Blöcke überlappen sich nicht rechtzeitig. Wenn sich überlappende Elemente in einem Kalender befinden, werden diese Elemente von Outlook zusammengeführt, um sich nicht überschneidende frei/gebucht-Blöcke in der Enumeration zu bilden, die auf dieser Rangfolge basieren: Abwesenheit, gebucht, mit Vorbehalt. 
  
Zum Registrieren des frei/gebucht-Anbieters in Outlook sollte der e-Mail-Anbieter folgende Schritte ausführen:
  
1. Registrieren des frei/gebucht-Anbieters mit COM, Bereitstelleneiner CLSID, die den Zugriff auf die Implementierung von **IFreeBusySupport**durch den Anbieter ermöglicht. 
    
2. Lassen Sie Outlook wissen, dass der frei/gebucht-Anbieter vorhanden ist, indem Sie `<xx.x>` den folgenden Schlüssel (wobei die Version von Outlook darstellt) in der Systemregistrierung festlegen: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Wenn der Transportanbieter beispielsweise SMTP ist, um den Anbieter bei Microsoft Outlook 2010 zu registrieren, legen Sie den folgenden Schlüssel auf die Daten in der folgenden Tabelle fest: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Name |Typ |Wert |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID für die jeweilige Implementierung von IFreeBusySupport}  |
   
   In diesem Szenario erstellt Outlook die COM-Klasse und verwendet Sie zum Abrufen von Frei/Gebucht-Informationen für beliebige SMTP-e-Mail-Benutzer.
    
Um ein Adressbuch und einen Transportanbieter zu unterstützen, die einen anderen Adresseintragstyp als SMTP verwenden, ändern Sie den *Namen* entsprechend. 
  
> [!NOTE]
> Während der Installation sollten frei/gebucht-Anbieter überprüfen, ob eine Registrierungseinstellung für den gleichen Adresseintragstyp bereits vorhanden ist. Wenn dies der Fall ist, sollte der frei/gebucht-Anbieter den aktuellen Anbieter für diesen Adresseintragstyp überschreiben und bei Deinstallationen bei diesem Anbieter wiederherstellen. Wenn jedoch ein Benutzer mehr als einen frei/gebucht-Anbieter für denselben Adresseintragstyp installiert hat, sollte der Benutzer diese Anbieter in der umgekehrten Reihenfolge deinstallieren (also immer den aktuellen Anbieter deinstallieren). Andernfalls kann die Registrierung auf einen Anbieter verweisen, der bereits deinstalliert wurde. 
  
## <a name="api-components"></a>API-Komponenten

Die Frei/Gebucht-API umfasst die folgenden Komponenten:
  
### <a name="definitions"></a>Definitionen

- [Konstanten (frei/gebucht-API)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Datentypen

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Schnittstellen

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

