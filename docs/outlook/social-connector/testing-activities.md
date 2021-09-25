---
title: Testen von Aktivitäten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Anbieter von Outlook Connector für soziale Netzwerke (OSC) die On-Demand-Synchronisierung verwendet, um Aktivitäten von Freunden und Nicht-Freunden ordnungsgemäß zurückzugeben.
ms.openlocfilehash: 63ddee94e28e7b8dfcb5d616069df2c275d41587
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582988"
---
# <a name="testing-activities"></a>Testen von Aktivitäten

In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Anbieter von Outlook Connector für soziale Netzwerke (OSC) die On-Demand-Synchronisierung verwendet, um Aktivitäten von Freunden und Nicht-Freunden ordnungsgemäß zurückzugeben.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>On-Demand-Synchronisierung

Ein OSC-Anbieter implementiert **ISocialProvider::GetCapabilities**, die der OSC aufruft, um zu bestimmen, ob der Anbieter die On-Demand-Synchronisierung von Aktivitäten von Freunden und Nicht-Freunden unterstützt. Für die im Outlook Personenbereich angezeigten Personen ruft der OSC ihre SMTP-Adressen ab und hashet diese, ruft [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)auf und speichert (im Arbeitsspeicher) die für diese Personen zurückgegebenen Aktivitätendaten. 
  
### <a name="determining-activities-to-get"></a>Ermitteln der abzurufenden Aktivitäten

Die an **GetActivitiesEx übergebenen** SMTP-Hashadressen sind der Schlüssel, um zu bestimmen, ob der OSC Aktivitäten für einen Freund oder einen Nicht-Freund erhält. Der OSC ruft Aktivitäten für eine Person ab, wenn die Person diese SMTP-Adresse in ihrem Konto in einem sozialen Netzwerk angibt. Wenn die Person diese SMTP-Adresse nicht in ihr Konto im sozialen Netzwerk einschließt oder wenn diese Person ein Freund ist, aber von einer anderen E-Mail-Adresse im sozialen Netzwerk stammt, erhält **GetActivitiesEx** keine Aktivitäten für diese Person. Außerdem enthalten die zurückgegebenen Daten für eine Person, die kein Freund ist, aber die SMTP-Adressen in ihrem Konto in ihrem sozialen Netzwerk angibt, nur das, was einem Nicht-Freund gemäß den Datenschutzeinstellungen dieser Person zur Verfügung steht. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Erstellen von Testfächern für Freunde und Nicht-Freunde

Um einen Testbeantragsteller für einen Freund zu erstellen, identifizieren Sie die SMTP-Adresse einer Person, die diese Adresse in sein Konto in einem sozialen Netzwerk einschließt und die einen Freundesstatus mit dem angemeldeten Benutzer in diesem Netzwerk hat. Erstellen Sie eine E-Mail-Nachricht, die diese SMTP-Adresse enthält. Um einen Testantrag für einen Nicht-Freund zu erstellen, identifizieren Sie auf ähnliche Weise die SMTP-Adresse einer Person, die kein Freund des angemeldeten Benutzers ist, anhand dieser Adresse und die in ihren Datenschutzeinstellungen angegeben hat, damit Nicht-Freunde ihr Profil im sozialen Netzwerk anzeigen können. Erstellen Sie eine E-Mail-Nachricht, die diese SMTP-Adresse enthält. 
  
Wenn Sie im Outlook Explorer die E-Mail-Nachricht auswählen, die einen Freund (oder einen Nicht-Freund) enthält, werden im Personenbereich die Empfänger angezeigt. Wenn Sie den Freund (oder Nicht-Freund) im Personenbereich auswählen, können Sie testen, ob der Anbieter Informationen über die Person bereitstellt.
  
### <a name="test-scenarios"></a>Testszenarien

Um zu überprüfen, ob Sie geeignete Aktivitäten für Freunde und Nicht-Freunde erhalten, testen Sie die folgenden Szenarien.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Die im Personenbereich ausgewählte Person ist ein Freund des angemeldeten Benutzers im sozialen Netzwerk.  <br/> |Im Personenbereich werden das Profil und das Profilbild dieser Person angezeigt, wie im sozialen Netzwerk veröffentlicht.  <br/> |
|Die im Personenbereich ausgewählte Person ist ein Nicht-Freund des angemeldeten Benutzers im sozialen Netzwerk, hat es jedoch zugelassen, dass sein Profil von Nicht-Freunden angezeigt wird.  <br/> |Im Personenbereich werden das Profil und das Profilbild dieser Person angezeigt, wie im sozialen Netzwerk veröffentlicht.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

