---
title: Abrufen von Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: Das osc bilden die ISocialProvider::GetCapabilities-Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen.
ms.openlocfilehash: 82bb5322118fa3ebd7610f56b8f34ae95b59a40f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795955"
---
# <a name="getting-activities"></a>Abrufen von Aktivitäten

Das osc bilden die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen. **GetActivities** und **DynamicActivitiesLookupEx** Elemente in der zurückgegebenen **Funktionen** XML angeben, dass der OSC-Anbieter erste Aktivitäten bei Bedarf und Speichern von Aktivitäten im Arbeitsspeicher unterstützt, kann die OSC Folgendes machen. Sequenz aufrufen. Die OSC Notizen auch die Hash-Funktion in die **Funktionen** XML im **HashFunction** -Element angegeben. Die OSC-Methoden in der folgenden Reihenfolge Aktivitäten und Informationen abrufen (wie durch die [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle unterstützt) für Freunde und Familie im sozialen Netzwerk Anrufe: 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) – am Ende des Authentifizierungsprozesses, ruft der OSC **GetLoggedOnUser** zum Abrufen einer [ISocialProfile](isocialprofileisocialperson.md) -Schnittstelle für den Benutzer authentifiziert wird. Weitere Informationen zur Authentifizierung finden Sie unter [Standardauthentifizierung](basic-authentication.md) und [formularbasierte Authentifizierung](forms-based-authentication.md).
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) – für die Personen, die Sie im Bereich Personen Outlook angezeigt, die OSC abruft und Hashes ihre SMTP-Adressen, ruft **ISocialSession2::GetActivitiesEx**und speichert (im Arbeitsspeicher) die Aktivitäten Daten für zurückgegeben Diese Personen. Die OSC ruft in einen Ausgabeparameter, _Aktivitäten_, also eine Zeichenfolge, die eine Auflistung von Aktivitäten für Freunde des angemeldeten Benutzers enthält. Diese Zeichenfolge entspricht der Schemadefinition für das **ActivityFeed** -Element. 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) – für jedes **ActivityDetails** -Element in der **ActivityFeed** von **GetActivitiesEx**zurückgegebenen XML-Daten ein, der angibt, die Person, die diese Aktivität besitzt **OwnerID** -Element vorhanden ist. Die OSC verwendet diesen **OwnerID** Wert CSEs **GetPerson** um eine **ISocialPerson** -Schnittstelle für diese Person zu erhalten. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) – basierend auf dem **ISocialPerson** -Objekt, das Sie in Schritt 3 abgerufen, ruft der OSC **GetDetails** um Details für diese Person an, wie beispielsweise vor- und Nachnamen zu erhalten. Das osc bilden kann auch für jede Aktivität in ein **ActivityDetails** -Element in der **ActivityFeed** in Schritt 2 von **GetActivitiesEx** zurückgegebenen XML-Daten vornehmen. 
    
> [!NOTE]
> Die OSC wird der Aktivitätencache standardmäßig in Abständen aktualisiert. Weitere Informationen zum Aktualisieren des Caches Aktivitäten finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Siehe auch

- [XML-Code für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

