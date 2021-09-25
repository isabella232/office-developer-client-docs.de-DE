---
title: Abrufen von Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: Der OSC ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: c1d34913a372c3959b34322eadf9964dcbbeb054
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590457"
---
# <a name="getting-activities"></a>Abrufen von Aktivitäten

Der OSC ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln. Wenn die **Elemente "getActivities"** und **"dynamicActivitiesLookupEx"** in der zurückgegebenen **Funktions-XML** angeben, dass der OSC-Anbieter das Abrufen von Aktivitäten bei Bedarf und das Speichern von Aktivitäten im Arbeitsspeicher unterstützt, kann osc die folgende Aufrufsequenz vornehmen. Der OSC notiert auch die Hashfunktion, die im **hashFunction-Element** in der **Funktions-XML** angegeben ist. Der OSC ruft Methoden in der folgenden Sequenz auf, um Aktivitäten und Informationen (wie von der [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) unterstützt) für Freunde und Nicht-Freunde im sozialen Netzwerk abzurufen: 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) - Am Ende des Authentifizierungsprozesses ruft der OSC **GetLoggedOnUser auf,** um eine [ISocialProfile-Schnittstelle](isocialprofileisocialperson.md) für den benutzer abzurufen, der authentifiziert wird. Weitere Informationen zur Authentifizierung finden Sie unter ["Standardauthentifizierung"](basic-authentication.md) und ["Formularbasierte Authentifizierung".](forms-based-authentication.md)
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) - Für die im Outlook Personenbereich angezeigten Personen ruft osc ihre SMTP-Adressen ab und hashet diese, ruft **ISocialSession2::GetActivitiesEx** auf und speichert (im Speicher) die für diese Personen zurückgegebenen Aktivitätendaten. Der OSC ruft den Ausgabeparameter  _"activities"_ ab, d. h. eine Zeichenfolge, die eine Sammlung von Aktivitäten für Freunde des angemeldeten Benutzers enthält. Diese Zeichenfolge entspricht der Schemadefinition für das **activityFeed-Element.** 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) -Für jedes **activityDetails-Element** in der von **GetActivitiesEx zurückgegebenen** **activityFeed-XML** gibt es ein **ownerID-Element,** das die Person angibt, der diese Aktivität gehört. Der OSC verwendet diesen **ownerID-Wert,** um **GetPerson** aufzurufen, um eine **ISocialPerson-Schnittstelle** für diese Person abzurufen. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) - Basierend auf dem aus Schritt 3 abgerufenen **ISocialPerson-Objekt** ruft der OSC **GetDetails** auf, um Details für diese Person wie Vorname und Nachname abzurufen. Das OSC kann dasselbe für jede Aktivität ausführen, die in einem **activityDetails-Element** in der **activityFeed** XML angegeben ist, die von **GetActivitiesEx** in Schritt 2 zurückgegeben wird. 
    
> [!NOTE]
> Der OSC aktualisiert den Aktivitätencache in einem Standardintervall. Weitere Informationen zum Aktualisieren des Aktivitätencaches finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

