---
title: Testen von Aktivitäten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: In diesem Thema wird beschrieben, Tests und Szenarien, um sicherzustellen, dass der Anbieter Outlook Social Connector (OSC) bedarfsgesteuerten Synchronisierung verwendet, um Aktivitäten Freunde und nicht Freunde entsprechend zurückzugeben.
ms.openlocfilehash: 82d24b106e8d429d20a2d396eb60155cbb95f91f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796089"
---
# <a name="testing-activities"></a>Testen von Aktivitäten

In diesem Thema wird beschrieben, Tests und Szenarien, um sicherzustellen, dass der Anbieter Outlook Social Connector (OSC) bedarfsgesteuerten Synchronisierung verwendet, um Aktivitäten Freunde und nicht Freunde entsprechend zurückzugeben.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Bedarfsgesteuerte Synchronisierung

Ein OSC-Anbieter implementiert **ISocialProvider::GetCapabilities**, die die OSC aufruft, um zu bestimmen, ob der Anbieter bedarfsgesteuerten Synchronisierung von Aktivitäten Freunde und Freunde-nicht unterstützt. Für die Personen, die im Bereich Personen Outlook angezeigt wird erhält der OSC und Hashes, die Ihre SMTP-Adressen, ruft [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)und speichert (im Arbeitsspeicher) die Aktivitäten Daten, für diese Personen zurückgegeben. 
  
### <a name="determining-activities-to-get"></a>Bestimmen der abzurufenden Aktivitäten

Hash SMTP-Adressen an **GetActivitiesEx** übergeben werden die Taste, um zu bestimmen, ob die OSC Aktivitäten für einen Freund oder nicht Friend relevanten Informationen erhalten. Die OSC ruft Aktivitäten für eine Person, wenn die Person, SMTP-Adresse in seinem für soziale Netzwerkkonto angibt. Wenn die Person nicht die SMTP-Adresse in seinem sozialen Netzwerk-Konto umfasst oder wenn die Person einen Freund ist jedoch durch eine andere e-Mail-Adresse im sozialen Netzwerk **GetActivitiesEx** keine Aktivitäten für diese Person erhält. Darüber hinaus enthält für eine Person, ist nicht mit einem Freund, gibt die SMTP-Adressen in seinem sozialen Netzwerk-Konto, die zurückgegebenen Daten nur an einen nicht-Freund, wie durch die datenschutzeinstellungen der betreffenden Person zugelassen verfügbar sind. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Erstellen von Test-Themen für Freunde und nicht Freunde

So erstellen Sie einen Test Betreff für einen Freund, identifizieren Sie die SMTP-Adresse einer Person, die diese Adresse enthält, in Konto für soziale Netzwerke und wer hat einen Freund Status mit der angemeldete Benutzer auf das Netzwerk. Erstellen Sie eine e-Mail-Nachricht, die diese SMTP-Adresse enthält. So erstellen Sie einen Test Betreff für einen Freund, identifizieren Sie entsprechend die SMTP-Adresse einer Person, die keinen Freund des angemeldeten Benutzers von dieser Adresse, und angegeben, die in seinem datenschutzeinstellungen auf nicht-Freunde an ihr Profil im sozialen Netzwerk zulassen. Erstellen Sie eine e-Mail-Nachricht, die diese SMTP-Adresse enthält. 
  
Wenn Sie die e-Mail-Nachricht auswählen, die ein Friend (oder nicht Friend) enthält, zeigt den Bereich Personen im Outlook-Explorer die Empfänger an. Auswählen der Friend (oder nicht Friend) im Bereich Personen können Sie testen, dass der Anbieter, Informationen über die Person bereitstellt.
  
### <a name="test-scenarios"></a>Testszenarien

Testen Sie zum bestätigen, dass Sie entsprechende Aktivitäten für Freunde und nicht Freunde abrufen, für die folgenden Szenarien.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Person, die Sie im Bereich Personen ausgewählt ist ein Freund mit dem angemeldeten Benutzer im sozialen Netzwerk.  <br/> |Bereich Personen werden diese Person Profil und Profilbild wie im sozialen Netzwerk gebucht angezeigt.  <br/> |
|Person, die Sie im Bereich Personen ausgewählt ist ein nicht-Freund des angemeldeten Benutzers im sozialen Netzwerk, jedoch hat zulässig seinem Profil nicht Freunde anzeigen können.  <br/> |Bereich Personen werden diese Person Profil und Profilbild wie im sozialen Netzwerk gebucht angezeigt.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML-Code für Aktivitäten](xml-for-activities.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

