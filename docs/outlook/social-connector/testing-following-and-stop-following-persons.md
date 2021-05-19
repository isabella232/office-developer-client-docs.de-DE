---
title: Testen des Folgens von Personen und Beenden des Folgens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: In diesem Thema werden Szenarien beschrieben, um die Fähigkeit des Outlook Social Connector (OSC) zu testen, einem Freund zu folgen und aufzuhören, einem Freund im sozialen Netzwerk zu folgen.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432450"
---
# <a name="testing-following-and-stop-following-persons"></a>Testen des Folgens von Personen und Beenden des Folgens

In diesem Thema werden Szenarien beschrieben, um die Fähigkeit des Outlook Social Connector (OSC) zu testen, einem Freund zu folgen und aufzuhören, einem Freund im sozialen Netzwerk zu folgen.
  
## <a name="following-a-person"></a>Folgen einer Person

Um einer Person zu folgen, fügen Sie eine Person als Freund im sozialen Netzwerk hinzu, indem Sie die smtp-Adresse verwenden, die vom ausgewählten element Outlook wird. Das Folgen einer Person in einem sozialen Netzwerk umfasst in der Regel das Anfordern einer Berechtigung von dieser Person per E-Mail an diese SMTP-Adresse. Um die Berechtigung zu erteilen, muss diese Person entweder über diese SMTP-Adresse verfügen, die bereits in ihrem Konto für soziale Netzwerke enthalten ist, oder sie muss bereit sein, diesen SMTP einem Konto des sozialen Netzwerks hinzuzufügen. Testen Sie jedes der folgenden Szenarien, um zu überprüfen, ob sich Ihr OSC-Anbieter ordnungsgemäß verhält.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Versucht, einer Person im sozialen Netzwerk zu folgen, die im sozialen Netzwerk vorhanden ist.  <br/> |Für ein soziales Netzwerk, das keine Berechtigung von der Person benötigt, fügt das soziale Netzwerk die Person sofort als Freund hinzu.  <br/> Für ein Netzwerk, für das die Berechtigung dieser Person erforderlich ist, sendet das soziale Netzwerk eine Benachrichtigung. Im Outlook Personenbereich wird ein ausstehendes Symbol für diese Person angezeigt.  <br/> |
|Versucht, einer Person im sozialen Netzwerk zu folgen, die nicht im sozialen Netzwerk vorhanden ist.  <br/> |Der OSC-Anbieter zeigt den entsprechenden Fehler in [ISocialSession::FollowPerson](isocialsession-followperson.md) oder [ISocialSession2::FollowPersonEx an.](isocialsession2-followpersonex.md)  <br/> |
|Einem Freund im sozialen Netzwerk folgen.  <br/> |Für den im Bereich Personen ausgewählten Freund werden das Signal des sozialen Netzwerks und das Profilbild des Freundes für dieses soziale Netzwerk angezeigt.  <br/> |
|Auswählen des Links zur Profilseite eines Freundes.  <br/> |Die Seite des Freundes im sozialen Netzwerk wird im Standardbrowser des angemeldeten Benutzers geöffnet.  <br/> |
   
## <a name="stop-following-a-person"></a>Beenden der Folgen einer Person

Wenn Sie die Folgen einer Person beenden möchten, entfernen Sie diese Person als Freund im sozialen Netzwerk. Testen Sie das folgende Szenario, um zu überprüfen, ob Ihr OsC-Anbieter nicht mehr ordnungsgemäß einer Person folgt.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Versucht, eine Person als Freund im sozialen Netzwerk zu entfernen.  <br/> |Das soziale Netzwerk listet diese Person nicht mehr als Freund auf dem Konto des angemeldeten Benutzers auf.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

