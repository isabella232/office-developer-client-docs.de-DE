---
title: Implementieren von Sicherheitsmaßnahmen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c2926e7c94178d5a3135f34e2ab3b3ae11d145dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568483"
---
# <a name="implementing-security"></a>Implementieren von Sicherheitsmaßnahmen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn das messaging-System erforderlich sind, ist der Adressbuchhierarchie verantwortlich für die Implementierung der Sicherheit für den Zugriff auf die messaging-System einer angemessene Lautstärke. Jedes ein- oder ausgehende Nachricht über einen Transportanbieter durch die MAPI-Warteschlange wird im Zusammenhang mit einer Sitzung Anbieter behandelt. Der Adressbuchhierarchie kann ein Anmeldedialogfeld für den Benutzer angezeigt, die für die Anmeldeinformationen des Benutzers aufgefordert werden, bevor er eine solche Verbindung. Alternativ kann der Adressbuchhierarchie zuvor eingegebenen Anmeldeinformationen des Benutzers im Bereich diese Eigenschaft in einem Profilabschnitt speichern und verwenden sie für den Zugriff ohne Bestätigung.
  
Berücksichtigen Sie beim Implementieren von Ihrer Adressbuchhierarchie Sicherheit Folgendes:
  
- Mit mehreren installierten Dienstanbieter können eine Vielzahl von Namen und Kennwörter, die einem Benutzer zugeordnet werden.
    
- MAPI ermöglicht mehrerer Sitzungen mit mehreren Identitäten. Anbieter werden empfohlen, die Unterstützung mehrerer Sitzungen aber nicht dazu erforderlich sind.
    
- Jede Sitzung mit eines Transportdienstes ist MAPI einen getrennten Abschnitt im Profil des Benutzers zugeordnet. Der Transportdienst kann die [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode verwenden, den Zugriff auf die in diesem Abschnitt, die verwendet werden kann, um alle Informationen im Zusammenhang mit dieser Sitzung, einschließlich der Anmeldeinformationen zu speichern. 
    
- Mit mehreren Anbietern installierten Transport gilt es nicht unbedingt, dass der Benutzer nur eine einzelne e-Mail-Adresse verfügt. Ein Benutzer kann eine separate e-Mail-Adresse für jeden Transportanbieter installierten haben oder eine andere Adresse für jede Sitzung auf einen einzigen Anbieter aufweisen kann.
    
Weitere Informationen zum Speichern von Anmeldeinformationen in Profil Abschnitten finden Sie unter [Message-Dienste und -Profilen](message-services-and-profiles.md) und [IProfSect: IMAPIProp](iprofsectimapiprop.md).
  

