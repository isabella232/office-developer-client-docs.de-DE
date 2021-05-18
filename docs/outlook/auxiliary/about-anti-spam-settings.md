---
title: Informationen zu Anti-Spam-Einstellungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook können Benutzer Einstellungen für jedes Konto angeben, um das Konto vor Spam zu schützen. Solche Antispameinstellungen werden in einem Abschnitt gespeichert, der für dieses Konto im Benutzerprofil festgelegt ist.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316961"
---
# <a name="about-anti-spam-settings"></a>Informationen zu Anti-Spam-Einstellungen

Outlook können Benutzer Einstellungen für jedes Konto angeben, um das Konto vor Spam zu schützen. Solche Antispameinstellungen werden in einem Abschnitt gespeichert, der für dieses Konto im Benutzerprofil festgelegt ist. Verwenden Sie [die PROP_ACCT_PREFERENCES_UID-Eigenschaft,](prop_acct_preferences_uid.md) um die eindeutige ID (UID) für den Abschnitt im Profil zu erhalten, in dem die Einstellungen des Benutzers für dieses Konto gespeichert sind, einschließlich der Antispameinstellungen. 
  
Verwenden Sie die folgenden Eigenschaften, um Antispameinstellungen für das Konto zu erhalten:
  
- [PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)– Gibt eine durch Semikolons getrennte Liste von E-Mail-Adressen und Domänen an, die der Benutzer als blockierte Absender für das Konto angegeben hat.
    
- [PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)– Gibt die Spamfilterungsstufe an, die der Benutzer für das Konto angegeben hat. In der folgenden Tabelle sind die unterstützten Werte aufgeführt.
    
|Unterstützter Wert |Definition |
|:-----|:-----|
|Keine  <br/> |0xFFFFFFFF  <br/> |
|Niedrig  <br/> |0x00000006  <br/> |
|Mittel  <br/> |0x00000005  <br/> |
|Hoch  <br/> |0x00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)– Gibt eine durch Semikolons getrennte Liste von E-Mail-Adressen und Domänen an, die der Benutzer als vertrauenswürdige Empfänger für das Konto angegeben hat.
    
- [PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)– Gibt eine durch Semikolons getrennte Liste von E-Mail-Adressen und Domänen an, die der Benutzer als vertrauenswürdige Absender für das Konto angegeben hat.
    
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Hinzufügen von Namen zu junk-E-Mail-Filterlisten](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

