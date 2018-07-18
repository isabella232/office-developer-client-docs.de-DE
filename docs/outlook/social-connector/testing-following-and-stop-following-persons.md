---
title: Testen des Folgens von Personen und Beenden des Folgens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: In diesem Thema werden die Szenarien zum Testen des Outlook Social Connector (OSC)-Anbieters Möglichkeit, führen einen Freund, und beenden Sie einen Freund auf dem sozialen Netzwerk folgen.
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796078"
---
# <a name="testing-following-and-stop-following-persons"></a>Testen des Folgens von Personen und Beenden des Folgens

In diesem Thema werden die Szenarien zum Testen des Outlook Social Connector (OSC)-Anbieters Möglichkeit, führen einen Freund, und beenden Sie einen Freund auf dem sozialen Netzwerk folgen.
  
## <a name="following-a-person"></a>Nach einer Person

Um eine Person folgen werden eine Person als Freund im sozialen Netzwerk, die SMTP-Adresse zur Verfügung gestellt, durch das ausgewählte Outlook-Element hinzugefügt. Nach einer Person in der Regel in einem sozialen Netzwerk umfasst anfordern Berechtigung von dieser Person per e-Mail an diese SMTP-Adresse. Um die Berechtigung zu erteilen, die Person muss entweder haben, SMTP-Adresse, die bereits in seinem für soziale Netzwerkkonto enthalten oder bereit sind, hinzufügen, SMTP in ein Konto für soziale Netzwerke. Testen Sie die folgenden Szenarien stellen Sie sicher, dass Ihre OSC-Anbieter richtig funktioniert.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Beim Versuch, führen eine Person auf soziale Netzwerke, die im sozialen Netzwerk vorhanden ist.  <br/> |Für ein social Network, die keine Berechtigung, die von der Person erforderlich ist, fügt den Benutzer als Freund sofort für soziale Netzwerke hinzu.  <br/> Für ein Netzwerk, die von dieser Person die Berechtigung benötigt, sendet das soziale Netzwerk eine Benachrichtigung. Bereich Personen Outlook eine ausstehende Symbol für diese Person angezeigt.  <br/> |
|Beim Versuch, führen eine Person auf soziale Netzwerke, die nicht im sozialen Netzwerk vorhanden ist.  <br/> |Der OSC-Anbieter den entsprechenden Fehler in [ISocialSession::FollowPerson](isocialsession-followperson.md) oder [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)angezeigt.  <br/> |
|Auf dem sozialen Netzwerk einen Freund folgen.  <br/> |Für die Friend im Bereich Personen ausgewählt ist werden dem sozialen Netzwerk-Logo und die Friend Profil Teile des Bildes für das soziale Netzwerk angezeigt.  <br/> |
|Die Verknüpfung auf der Profilseite des einen Freund auswählen.  <br/> |Die Friend-Seite im sozialen Netzwerk im Standardbrowser des angemeldeten Benutzers wird geöffnet.  <br/> |
   
## <a name="stop-following-a-person"></a>Beenden Sie nach einer person

Um nach einer Person zu beenden ist diese Person als Freund im sozialen Netzwerk zu entfernen. Testen Sie das folgende Szenario, um Ihre OSC-Anbieter wird beendet, die nach einer Person ordnungsgemäß zu überprüfen.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Versucht, eine Person als Freund im sozialen Netzwerk zu entfernen.  <br/> |Soziale Netzwerke werden nicht mehr die Person als Freund Konto des angemeldeten Benutzers aufgelistet.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

