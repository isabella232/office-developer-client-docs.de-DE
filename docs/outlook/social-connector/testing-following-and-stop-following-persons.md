---
title: Testen des Folgens von Personen und Beenden des Folgens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: In diesem Thema werden Szenarien zum Testen der Funktion des Outlook Social Connector (OSC)-Anbieters zum Folgen eines Freundes und zum Beenden des Nachschlagens eines Freundes im sozialen Netzwerk beschrieben.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432450"
---
# <a name="testing-following-and-stop-following-persons"></a>Testen des Folgens von Personen und Beenden des Folgens

In diesem Thema werden Szenarien zum Testen der Funktion des Outlook Social Connector (OSC)-Anbieters zum Folgen eines Freundes und zum Beenden des Nachschlagens eines Freundes im sozialen Netzwerk beschrieben.
  
## <a name="following-a-person"></a>Nach einer Person

Um einer Person zu folgen, wird eine Person als Freund im sozialen Netzwerk unter Verwendung der vom ausgewählten Outlook-Element bereitgestellten SMTP-Adresse hinzugefügt. Wenn Sie jemandem in einem sozialen Netzwerk folgen, wird in der Regel eine e-Mail an diese SMTP-Adresse angefordert. Um die Berechtigung erteilen zu können, muss diese Person entweder über diese SMTP-Adresse verfügen, die bereits in Ihrem sozialen Netzwerkkonto enthalten ist, oder bereit sein, diesen SMTP-Account zu einem sozialen Netzwerkkonto hinzuzufügen. Testen Sie jedes der folgenden Szenarien, um sicherzustellen, dass der OSC-Anbieter ordnungsgemäß verhält.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Sie versuchen, einer Person im sozialen Netzwerk zu folgen, die im sozialen Netzwerk vorhanden ist.  <br/> |Für ein soziales Netzwerk, das keine Berechtigung von der Person benötigt, fügt das soziale Netzwerk die Person sofort als Freund hinzu.  <br/> Für ein Netzwerk, das eine Berechtigung von dieser Person benötigt, sendet das soziale Netzwerk eine Benachrichtigung. Der Outlook-Personen Bereich zeigt ein ausstehende Symbol für diese Person an.  <br/> |
|Sie versuchen, einer Person im sozialen Netzwerk zu folgen, die nicht im sozialen Netzwerk vorhanden ist.  <br/> |Der OSC-Anbieter zeigt den entsprechenden Fehler in [ISocialSession:: FollowPerson](isocialsession-followperson.md) oder [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md)an.  <br/> |
|Nach einem Freund im sozialen Netzwerk.  <br/> |Für den im Personen Bereich ausgewählten Freund werden das Abzeichen des sozialen Netzwerks und das Profilbild des Freundes für dieses soziale Netzwerk angezeigt.  <br/> |
|Auswählen des Links zur Profilseite eines Freundes.  <br/> |Die Seite des Freundes im sozialen Netzwerk wird im Standardbrowser des angemeldeten Benutzers geöffnet.  <br/> |
   
## <a name="stop-following-a-person"></a>Nach einer Person anhalten

So beenden Sie das Folgen einer Person ist, diese Person als Freund im sozialen Netzwerk zu entfernen. Testen Sie das folgende Szenario, um zu überprüfen, ob Ihr OSC-Anbieter beendet, eine Person ordnungsgemäß zu folgen
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Sie versuchen, eine Person als Freund im sozialen Netzwerk zu entfernen.  <br/> |Das soziale Netzwerk listet diese Person nicht mehr als Freund im Konto des angemeldeten Benutzers auf.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

