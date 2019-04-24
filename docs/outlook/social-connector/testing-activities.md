---
title: Testen von Aktivitäten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: In diesem Thema werden Tests und Szenarien beschrieben, mit denen Sie sicherstellen können, dass der OSC-Anbieter (Outlook Social Connector) die on-Demand-Synchronisierung verwendet, um die Aktivitäten von Freunden und nicht-Freunden entsprechend zurückzugeben.
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329183"
---
# <a name="testing-activities"></a>Testen von Aktivitäten

In diesem Thema werden Tests und Szenarien beschrieben, mit denen Sie sicherstellen können, dass der OSC-Anbieter (Outlook Social Connector) die on-Demand-Synchronisierung verwendet, um die Aktivitäten von Freunden und nicht-Freunden entsprechend zurückzugeben.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Bedarfsgesteuerte Synchronisierung

Ein OSC-Anbieter implementiert **ISocialProvider:: getCapabilities**, die von OSC aufgerufen werden, um zu bestimmen, ob der Anbieter die bedarfsgesteuerte Synchronisierung von Aktivitäten von Freunden und nicht-Freunden unterstützt. Für die Personen, die im Outlook-Personen Bereich angezeigt werden, ruft OSC Ihre SMTP-Adressen ab, hasht Sie [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)und speichert (im Arbeitsspeicher) die für diese Personen zurückgegebenen Aktivitätsdaten. 
  
### <a name="determining-activities-to-get"></a>Bestimmen der zu erhaltenden Aktivitäten

Die an **GetActivitiesEx** übergebenen Hash-SMTP-Adressen sind der Schlüssel, um zu bestimmen, ob der osc Aktivitäten für einen Freund oder einen nicht-Freund erhält. OSC ruft Aktivitäten für eine Person ab, wenn die betreffende Person diese SMTP-Adresse in seinem sozialen Netzwerkkonto angibt. Wenn die betreffende Person diese SMTP-Adresse nicht in Ihrem sozialen Netzwerkkonto einschließt oder wenn diese Person ein Freund ist, aber durch eine andere e-Mail-Adresse im sozialen Netzwerk, **GetActivitiesEx** keine Aktivitäten für diese Person. Auch für eine Person, die kein Freund ist, aber die SMTP-Adressen in seinem sozialen Netzwerkkonto angibt, enthält die zurückgegebenen Daten nur das, was einem nicht-Freund gemäß den Datenschutzeinstellungen dieser Person zur Verfügung steht. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Erstellen von Testthemen für Freunde und nicht-Freunde

Wenn Sie einen Test Betreff für einen Freund erstellen möchten, identifizieren Sie die SMTP-Adresse einer Person, die diese Adresse in Ihrem sozialen Netzwerkkonto einschließt und die über einen Friend-Status mit dem angemeldeten Benutzer in diesem Netzwerk verfügt. Erstellen Sie eine e-Mail-Nachricht, die diese SMTP-Adresse enthält. Auf ähnliche Weise können Sie einen Test Betreff für einen nicht-Freund erstellen, indem Sie die SMTP-Adresse einer Person identifizieren, die von dieser Adresse nicht ein Freund des angemeldeten Benutzers ist, und die in Ihren Datenschutzeinstellungen angegeben hat, dass nicht-Freunden Ihr Profil im sozialen Netzwerk angezeigt werden kann. Erstellen Sie eine e-Mail-Nachricht, die diese SMTP-Adresse enthält. 
  
Wenn Sie im Outlook-Explorer die e-Mail-Nachricht auswählen, die einen Freund (oder nicht-Freund) enthält, werden im Bereich Personen die Empfänger angezeigt. Durch Auswählen des Freundes (oder nicht-Freundes) im Personen Bereich können Sie testen, ob der Anbieter Informationen zur Person bereitstellt.
  
### <a name="test-scenarios"></a>Testszenarien

Um zu überprüfen, ob Sie entsprechende Aktivitäten für Freunde und nicht-Freunde erhalten, testen Sie die folgenden Szenarien.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Person, die im Personen Bereich ausgewählt ist, ist ein Freund des angemeldeten Benutzers im sozialen Netzwerk.  <br/> |Im Bereich Personen werden die Profil-und Profil Bilder dieser Person angezeigt, die im sozialen Netzwerk veröffentlicht wurden.  <br/> |
|Person, die im Personen Bereich ausgewählt ist, ist ein nicht-Freund des angemeldeten Benutzers im sozialen Netzwerk, hat jedoch das Anzeigen des Profils durch nicht-Freunde ermöglicht.  <br/> |Im Bereich Personen werden die Profil-und Profil Bilder dieser Person angezeigt, die im sozialen Netzwerk veröffentlicht wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

