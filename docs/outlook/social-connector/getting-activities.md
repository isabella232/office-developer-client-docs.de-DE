---
title: Abrufen von Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: 'OSC Ruft die ISocialProvider:: getCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu bestimmen.'
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327188"
---
# <a name="getting-activities"></a>Abrufen von Aktivitäten

OSC Ruft die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode auf, um die Funktionen des osc-Anbieters für ein soziales Netzwerk zu bestimmen. Wenn die **GetActivities** -und **dynamicActivitiesLookupEx** -Elemente in den zurückgegebenen **Capabilities** -XML-Code darauf HINweisen, dass der osc-Anbieter Aktivitäten bei Bedarf unterstützt und Aktivitäten im Speicher speichert, kann osc folgende Aktionen ausführen: Aufrufsequenz. Der OSC stellt auch die im **hashFunction** -Element angegebene Hashfunktion im **Capabilities** -XML-Code fest. OSC ruft Methoden in der folgenden Reihenfolge auf, um Aktivitäten und Informationen (wie von der [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle unterstützt) für Freunde und nicht-Freunde im sozialen Netzwerk zu erhalten: 
  
1. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) – am Ende des Authentifizierungsprozesses ruft der osc **GetLoggedOnUser** auf, um eine [ISocialProfile](isocialprofileisocialperson.md) -Schnittstelle für den authentifizierten Benutzer abzurufen. Weitere Informationen zur Authentifizierung finden Sie unter [Standardauthentifizierung](basic-authentication.md) und [formularbasierte Authentifizierung](forms-based-authentication.md).
    
2. [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) – für die Personen, die im Outlook-Personen Bereich angezeigt werden, ruft osc Ihre SMTP-Adressen ab und hasht Sie **ISocialSession2:: GetActivitiesEx**und speichert (im Arbeitsspeicher) die zurückgegebenen Aktivitätsdaten für Diese Personen. OSC ruft in einem Output-Parameter, _Activities_, eine Zeichenfolge, die eine Auflistung von Aktivitäten für Freunde des angemeldeten Benutzers enthält. Diese Zeichenfolge entspricht der Schema Definition für das **activityFeed** -Element. 
    
3. [ISocialSession:: GetPerson](isocialsession-getperson.md) -für jedes **activityDetails** -Element im **activityFeed** -XML, das von **GetActivitiesEx**zurückgegeben wird, gibt es ein **Owner** -Element, das die Person angibt, die diese Aktivität besitzt. OSC verwendet diesen **Besitzer** -Wert zum Aufrufen von **GetPerson** , um eine **ISocialPerson** -Schnittstelle für diese Person abzurufen. 
    
4. [ISocialPerson:: getDetails](isocialperson-getdetails.md) – basierend auf dem **ISocialPerson** -Objekt, das aus Schritt 3 abgerufen wurde **** , ruft der osc getDetails auf, um Details für diese Person, wie den vor-und Nachnamen, abzurufen. OSC kann für jede in einem **activityDetails** -Element in der **activityFeed** -XML-Datei, die von **GetActivitiesEx** in Schritt 2 zurückgegeben wird, dasselbe tun. 
    
> [!NOTE]
> OSC aktualisiert den Aktivitäts Cache in einem Standardintervall. Weitere Informationen zum Aktualisieren des Aktivitäts Caches finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

