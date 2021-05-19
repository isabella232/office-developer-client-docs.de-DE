---
title: Abrufen von Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: Das OSC ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420577"
---
# <a name="getting-activities"></a>Abrufen von Aktivitäten

Das OSC ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln. Wenn die **Elemente getActivities** und **dynamicActivitiesLookupEx** im zurückgegebenen Funktionen-XML  angeben, dass der OSC-Anbieter das Abrufen von Aktivitäten bei Bedarf und das Speichern von Aktivitäten im Arbeitsspeicher unterstützt, kann das OSC die folgende Aufrufsequenz erstellen. Das OSC notiert auch die hash-Funktion, die im **hashFunction-Element** in der **Funktions-XML angegeben** ist. Das OSC ruft Methoden in der folgenden Reihenfolge auf, um Aktivitäten und Informationen (wie von der [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) unterstützt) für Freunde und Nicht-Freunde im sozialen Netzwerk zu erhalten: 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) – Am Ende des Authentifizierungsprozesses ruft das OSC **GetLoggedOnUser** auf, um eine [ISocialProfile-Schnittstelle](isocialprofileisocialperson.md) für den authentifizierten Benutzer zu erhalten. Weitere Informationen zur Authentifizierung finden Sie unter [Standardauthentifizierung](basic-authentication.md) und [formularbasierte Authentifizierung](forms-based-authentication.md).
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) – Für die Personen, die im Outlook-Personenbereich angezeigt werden, ruft das OSC seine #A0 ab und hasht diese, ruft **ISocialSession2::GetActivitiesEx** auf und speichert (im Arbeitsspeicher) die für diese Personen zurückgegebenen Aktivitätendaten. Das OSC ruft einen Ausgabeparameter,  _Aktivitäten_, ab, der eine Zeichenfolge ist, die eine Sammlung von Aktivitäten für Freunde des angemeldeten Benutzers enthält. Diese Zeichenfolge entspricht der Schemadefinition für das **activityFeed-Element.** 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) – Für jedes **activityDetails-Element** in der **activityFeed-XML,** die von **GetActivitiesEx** zurückgegeben wird, gibt es ein **ownerID-Element,** das die Person angibt, der diese Aktivität gehört. Das OSC verwendet diesen **ownerID-Wert,** um **GetPerson auf aufruft,** um eine **ISocialPerson-Schnittstelle** für diese Person zu erhalten. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) – Basierend auf dem **ISocialPerson-Objekt** aus Schritt 3 ruft das OSC **GetDetails** auf, um Details für diese Person zu erhalten, z. B. den Vor- und Nachnamen. Das OSC kann dasselbe für jede Aktivität tun, die in einem **activityDetails-Element** in der **activityFeed-XML** angegeben ist, die von **GetActivitiesEx** in Schritt 2 zurückgegeben wird. 
    
> [!NOTE]
> Das OSC aktualisiert den Aktivitätencache in einem Standardintervall. Weitere Informationen zum Aktualisieren des Aktivitätencaches finden Sie [unter Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

