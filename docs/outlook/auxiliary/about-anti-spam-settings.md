---
title: Informationen zu Anti-Spam-Einstellungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook ermöglicht Benutzern das Angeben von Einstellungen für jedes Konto das Konto vor Spam schützen. Eine solche Anti-Spam-Dateien werden in einem Abschnitt vorgesehen für dieses Konto im Profil des Benutzers gespeichert.
ms.openlocfilehash: 9d1ad6fcc0748d57dd71cb80460705fcd176fae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790910"
---
# <a name="about-anti-spam-settings"></a>Informationen zu Anti-Spam-Einstellungen

Outlook ermöglicht Benutzern das Angeben von Einstellungen für jedes Konto das Konto vor Spam schützen. Eine solche Anti-Spam-Dateien werden in einem Abschnitt vorgesehen für dieses Konto im Profil des Benutzers gespeichert. Verwenden Sie die [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) -Eigenschaft, um die eindeutige ID (UID) für den Abschnitt im Profil abzurufen, die Einstellungen für dieses Konto, einschließlich der Anti-Spam-Einstellungen des Benutzers gespeichert werden. 
  
Verwenden Sie die folgenden Eigenschaften, um Anti-Spam-Einstellungen für das Konto abzurufen:
  
- [PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)– gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen und Domänen, die der Benutzer als geblockten Absender für das Konto angegeben hat.
    
- [PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)– gibt die Ebene der Spam-filtern, die der Benutzer für das Konto angegeben hat. In der folgenden Tabelle sind die unterstützten Werte.
    
|Unterstützte Wert |Definition |
|:-----|:-----|
|Keine  <br/> |0xFFFFFFFF  <br/> |
|Low  <br/> |0 x 00000006  <br/> |
|Medium  <br/> |0 x 00000005  <br/> |
|High  <br/> |0 x 00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)– gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen und Domänen, die als vertrauenswürdige Empfänger für das Konto der Benutzer angegeben hat.
    
- [PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)– gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen und Domänen, die als vertrauenswürdige Absender für das Konto der Benutzer angegeben hat.
    
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Hinzufügen von Namen zu den Listen Junk-e-Mail-Filter](http://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

