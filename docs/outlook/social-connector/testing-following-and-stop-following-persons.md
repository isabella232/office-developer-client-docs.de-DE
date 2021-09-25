---
title: Testen des Folgens von Personen und Beenden des Folgens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: In diesem Thema werden Szenarien beschrieben, in denen die Fähigkeit des Anbieters Outlook Social Connector (OSC) getestet wird, einem Freund zu folgen und aufhört, einem Freund im sozialen Netzwerk zu folgen.
ms.openlocfilehash: 7d4051185d62240fd2fe3ca93a7e8bee3a4141d0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590359"
---
# <a name="testing-following-and-stop-following-persons"></a>Testen des Folgens von Personen und Beenden des Folgens

In diesem Thema werden Szenarien beschrieben, in denen die Fähigkeit des Anbieters Outlook Social Connector (OSC) getestet wird, einem Freund zu folgen und aufhört, einem Freund im sozialen Netzwerk zu folgen.
  
## <a name="following-a-person"></a>Folgen einer Person

Um einer Person zu folgen, müssen Sie eine Person als Freunde im sozialen Netzwerk hinzufügen, indem Sie die SMTP-Adresse verwenden, die vom ausgewählten Outlook Element bereitgestellt wird. Das Folgen einer Person in einem sozialen Netzwerk umfasst in der Regel das Anfordern einer Berechtigung von dieser Person durch eine E-Mail an diese SMTP-Adresse. Um die Berechtigung zu erteilen, muss diese Person entweder über die SMTP-Adresse verfügen, die bereits in ihrem Konto für soziale Netzwerke enthalten ist, oder sie muss bereit sein, diese SMTP einem Konto in einem sozialen Netzwerk hinzuzufügen. Testen Sie jedes der folgenden Szenarien, um zu überprüfen, ob sich Ihr OSC-Anbieter ordnungsgemäß verhält.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Versucht, einer Person im sozialen Netzwerk zu folgen, die im sozialen Netzwerk vorhanden ist.  <br/> |Für ein soziales Netzwerk, das keine Berechtigung von der Person benötigt, fügt das soziale Netzwerk die Person sofort als Freund hinzu.  <br/> Für ein Netzwerk, das die Berechtigung von dieser Person benötigt, sendet das soziale Netzwerk eine Benachrichtigung. Der Outlook Personenbereich zeigt ein ausstehendes Symbol für diese Person an.  <br/> |
|Versucht, einer Person im sozialen Netzwerk zu folgen, die nicht im sozialen Netzwerk vorhanden ist.  <br/> |Der OSC-Anbieter zeigt den entsprechenden Fehler in [ISocialSession::FollowPerson](isocialsession-followperson.md) oder [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)an.  <br/> |
|Einem Freund im sozialen Netzwerk folgen.  <br/> |Für den im Personenbereich ausgewählten Freund werden der Badge des sozialen Netzwerks und das Profilbild des Freundes für dieses soziale Netzwerk angezeigt.  <br/> |
|Auswählen des Links zur Profilseite eines Freundes.  <br/> |Die Seite des Freundes im sozialen Netzwerk wird im Standardbrowser des angemeldeten Benutzers geöffnet.  <br/> |
   
## <a name="stop-following-a-person"></a>Beenden des Folgens einer Person

Wenn Sie einer Person nicht mehr folgen möchten, entfernen Sie diese Person als Freunde im sozialen Netzwerk. Testen Sie das folgende Szenario, um sicherzustellen, dass Ihr OSC-Anbieter nicht mehr ordnungsgemäß einer Person folgt.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Versucht, eine Person als Freunde im sozialen Netzwerk zu entfernen.  <br/> |Das soziale Netzwerk listet diese Person nicht mehr als Freunde auf dem Konto des angemeldeten Benutzers auf.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

