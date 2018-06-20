---
title: Über die Frei/Gebucht-API
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Die Frei/Gebucht-API ermöglicht es e-Mail-Anbieter für Frei-/Gebucht-Status Informationen für den angegebenen Benutzerkonten innerhalb eines angegebenen Zeitraums.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790923"
---
# <a name="about-the-freebusy-api"></a>Über die Frei/Gebucht-API

Die Frei/Gebucht-API ermöglicht es e-Mail-Anbieter für Frei-/Gebucht-Status Informationen für den angegebenen Benutzerkonten innerhalb eines angegebenen Zeitraums. Der Frei/Gebucht-Status eines Textblocks Kalender des Benutzers ist einer der folgenden: Abwesenheits, gebucht, mit Vorbehalt oder frei.
  
## <a name="create-a-freebusy-provider"></a>Erstellen eines Anbieters für Frei/Gebucht-Informationen

Um Frei/Gebucht-Informationen an e-Mail-Benutzer zu ermöglichen, ein e-Mail-Anbieter einen Anbieter für Frei/Gebucht-Informationen erstellt und registriert sie bei Outlook. Der Frei/Gebucht-Anbieter muss die folgenden Schnittstellen implementieren. Beachten Sie, dass eine Anzahl von Elementen in diese Schnittstellen nicht unterstützt werden und muss zurückgeben, dass die angegebenen Werte zurückgeben. Insbesondere unterstützt die Frei/Gebucht-API nicht Schreibzugriff, um Frei/Gebucht-Informationen und Delegieren des Zugriffs auf Konten.
  
- [IFreeBusySupport](ifreebusysupport.md) – diese Schnittstelle unterstützt die Angabe der Schnittstellen, die Frei/Gebucht-Daten für bestimmte Benutzer zugreifen. [FBUser](fbuser.md) verwendet, um einen Benutzer zu identifizieren. 
    
- [IFreeBusyData](ifreebusydata.md) – diese Schnittstelle ruft ab und legt einen Zeitraum für einen bestimmten Benutzer fest und gibt eine Schnittstelle zum Aufzählen Datenblöcke Frei/Gebucht-Informationen in diesem Zeitraum zurück. Relative Zeit verwendet zum Abrufen und Festlegen der Zeitraum. Weitere Informationen finden Sie unter [Verwendung relative Zeit auf Frei/Gebucht-Daten zugreifen](how-to-use-relative-time-to-access-free-busy-data.md).
    
- [IEnumFBBlock](ienumfbblock.md) – diese Schnittstelle unterstützt den Zugriff auf und auflisten Datenblöcke Frei/Gebucht-Informationen für einen Benutzer innerhalb eines Zeitraums. 
    
   > [!NOTE]
   > Eine Enumeration enthält Frei/Gebucht-Blöcke, die den Frei/Gebucht-Status von Zeiträume Kalender des Benutzers, innerhalb eines Zeitraums (angegeben durch [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)) angeben. Elemente in einem Kalender, wie Termine und Besprechungsanfragen, bilden Blöcke in der-Aufzählung. Elemente, die im Kalender nebeneinander und haben den gleichen Frei/Gebucht-Status werden auf einem einzelnen Block Formular kombiniert. Ein freier Zeitraum in einem Kalender bildet auch einen Block. Keine zwei aufeinander folgenden Blöcke in einer Enumeration müssen daher den gleichen Frei/Gebucht-Status. Diese Blöcke überlappen nicht rechtzeitig. Wenn sich überschneidenden Elemente in einem Kalender sind, verbindet Outlook diese Elemente um Frei/Gebucht-Blöcke übereinander in der angegebenen Reihenfolge der Priorität-Enumeration bilden: Abwesenheits, gebucht, mit Vorbehalt. 
  
Zum Registrieren des Anbieters Frei/Gebucht-Informationen mit Outlook, sollte der e-Mail-Anbieter Folgendes ausführen:
  
1. Registrieren des Anbieters Frei/Gebucht-Informationen mit COM, bietet eine CLSID, die Zugriff auf den Anbieter Implementierung **IFreeBusySupport**ermöglicht. 
    
2. Lassen Sie Outlook wissen, dass der Anbieter Frei/Gebucht-Informationen vorhanden ist, indem Sie den folgenden Schlüssel festlegen (wobei `<xx.x>` steht für die Version von Outlook) in der Registrierung: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Beispielsweise ist der Adressbuchhierarchie SMTP, zum Registrieren des Anbieters mit Microsoft Outlook 2010, legen Sie den folgenden Schlüssel mit den Daten in der folgenden Tabelle: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Name |Typ |Wert |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID für die jeweilige Implementierung der IFreeBusySupport}  |
   
   In diesem Szenario wird Outlook gemeinsame erstellt die COM-Klasse und wird verwendet, um das Abrufen von Frei/Gebucht-Informationen für eine beliebige SMTP-Mail-Benutzer.
    
Ändern Sie den *Namen* entsprechend zur Unterstützung eines Adresse Adressbuch und Transport-Anbieters, die einen Eintrag Adresstyp als SMTP verwenden. 
  
> [!NOTE]
> Frei/Gebucht-Anbieter sollte während der Installation, überprüfen Sie, ob eine Einstellung in der Registrierung für den gleichen Adresstyp Eintrag bereits vorhanden ist. Wenn dies der Fall ist, sollte der Frei/Gebucht-Anbieter überschreiben den aktuellen Anbieter für diesen Eintrag Adresstyp und an diesen Anbieter wiederherstellen, wenn es deinstalliert. Jedoch, wenn ein Benutzer mehr als eine Frei/Gebucht-Anbieter für den gleichen Eintrag Adresstyp installiert wurde, der Benutzer sollte deinstallieren diese Anbieter in umgekehrter Reihenfolge als Installation (d. h., immer deinstallieren den neuesten Anbieter). Andernfalls kann die Registrierung für einen Anbieter verweist, die bereits deinstalliert wurde. 
  
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
    

