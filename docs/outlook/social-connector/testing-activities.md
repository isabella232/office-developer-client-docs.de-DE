---
title: Testen von Aktivitäten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Outlook Social Connector (OSC)-Anbieter die On-Demand-Synchronisierung verwendet, um Aktivitäten von Freunden und Nicht-Freunden entsprechend zurückzukehren.
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436300"
---
# <a name="testing-activities"></a>Testen von Aktivitäten

In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Outlook Social Connector (OSC)-Anbieter die On-Demand-Synchronisierung verwendet, um Aktivitäten von Freunden und Nicht-Freunden entsprechend zurückzukehren.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>On-Demand-Synchronisierung

Ein OSC-Anbieter implementiert **ISocialProvider::GetCapabilities**, das vom OSC aufruft, um zu bestimmen, ob der Anbieter die On-Demand-Synchronisierung von Aktivitäten von Freunden und Nicht-Freunden unterstützt. Für die Personen, die im Outlook-Personenbereich angezeigt werden, ruft das OSC seine #A0 ab und hasht sie, ruft [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)auf und speichert (im Arbeitsspeicher) die für diese Personen zurückgegebenen Aktivitätendaten. 
  
### <a name="determining-activities-to-get"></a>Bestimmen der zu erhaltenden Aktivitäten

Die hashierten SMTP-Adressen, die **an GetActivitiesEx** übergeben werden, sind der Schlüssel, um zu bestimmen, ob das OSC Aktivitäten für einen Freund oder einen Nichtfreund erhalten soll. Das OSC ruft Aktivitäten für eine Person ab, wenn die Person diese SMTP-Adresse in ihrem Konto für soziale Netzwerke angibt. Wenn die Person diese SMTP-Adresse nicht in ihr Konto für soziale Netzwerke einbekommt oder wenn es sich bei dieser Person um einen Freund, aber um eine andere E-Mail-Adresse im sozialen Netzwerk handelt, wird **getActivitiesEx** keine Aktivitäten für diese Person erhalten. Außerdem enthalten die zurückgegebenen Daten für eine Person, die kein Freund ist, aber die SMTP-Adressen in ihrem Konto für soziale Netzwerke angibt, nur das, was einem Nicht-Freund zur Verfügung steht, wie von den Datenschutzeinstellungen dieser Person zulässig. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Erstellen von Testthemen für Freunde und Nicht-Freunde

Um einen Testsubjekt für einen Freund zu erstellen, identifizieren Sie die SMTP-Adresse einer Person, die diese Adresse in ihr Konto für soziale Netzwerke ein schließt und über einen Freundesstatus mit dem angemeldeten Benutzer in diesem Netzwerk verfügt. Erstellen Sie eine E-Mail-Nachricht, die diese SMTP-Adresse enthält. Um einen Testbearbeiter für einen Nichtfreund zu erstellen, identifizieren Sie die SMTP-Adresse einer Person, die kein Freund des angemeldeten Benutzers ist, durch diese Adresse und die in ihren Datenschutzeinstellungen angegeben hat, dass Nicht-Freunde ihr Profil im sozialen Netzwerk anzeigen können. Erstellen Sie eine E-Mail-Nachricht, die diese SMTP-Adresse enthält. 
  
Wenn Sie Outlook E-Mail-Nachricht auswählen, die einen Freund (oder einen Nicht-Freund) enthält, zeigt der Personenbereich die Empfänger an. Wenn Sie den Freund (oder den Nicht-Freund) im Personenbereich auswählen, können Sie testen, ob der Anbieter Informationen über die Person zur Verfügung stellt.
  
### <a name="test-scenarios"></a>Testszenarien

Um sicherzustellen, dass Sie geeignete Aktivitäten für Freunde und Nicht-Freunde erhalten, testen Sie die folgenden Szenarien.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Die im Personenbereich ausgewählte Person ist ein Freund des angemeldeten Benutzers im sozialen Netzwerk.  <br/> |Der Personenbereich zeigt das Profil und Profilbild dieser Person an, wie im sozialen Netzwerk veröffentlicht.  <br/> |
|Die im Personenbereich ausgewählte Person ist ein Nichtfreund des angemeldeten Benutzers im sozialen Netzwerk, hat jedoch zugelassen, dass sein Profil von Nicht-Freunden angezeigt wird.  <br/> |Der Personenbereich zeigt das Profil und Profilbild dieser Person an, wie im sozialen Netzwerk veröffentlicht.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

