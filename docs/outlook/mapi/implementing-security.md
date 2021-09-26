---
title: Implementieren von Sicherheit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 52a8bb4c589e8d9e4c53e3ad8019204ba37e5b71
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620730"
---
# <a name="implementing-security"></a>Implementieren von Sicherheit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn das Messagingsystem dies erfordert, ist der Transportanbieter für die Implementierung eines geeigneten Sicherheitsniveaus für den Zugriff auf das Messagingsystem verantwortlich. Jede eingehende oder ausgehende Nachricht, die vom MAPI-Spooler über einen Transportanbieter gesendet wird, wird im Kontext einer Anbieteranmeldungssitzung verarbeitet. Der Transportanbieter kann dem Benutzer ein Anmeldedialogfeld anzeigen, in dem die Anmeldeinformationen eines Benutzers angefordert werden, bevor eine solche Verbindung hergestellt wird. Alternativ kann der Transportanbieter die zuvor eingegebenen Anmeldeinformationen des Benutzers im Bereich sicherer Eigenschaften innerhalb eines Profilabschnitts speichern und für den Zugriff ohne Aufforderung verwenden.
  
Berücksichtigen Sie bei der Implementierung der Sicherheit Ihres Transportanbieters Folgendes:
  
- Bei mehreren installierten Dienstanbietern kann eine Vielzahl von Namen und Kennwörtern mit einem Benutzer verknüpft sein.
    
- MAPI lässt mehrere Sitzungen mit mehreren Identitäten zu. Anbieter werden aufgefordert, mehrere Sitzungen zu unterstützen, müssen dies jedoch nicht tun.
    
- Jede Sitzung mit einem Transportanbieter wird von der MAPI einem separaten Abschnitt im Benutzerprofil zugeordnet. Der Transportanbieter kann die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) verwenden, um Zugriff auf diesen Abschnitt zu erhalten, der verwendet werden kann, um alle dieser Sitzung zugeordneten Informationen, einschließlich Anmeldeinformationen, zu speichern. 
    
- Bei mehreren installierten Transportanbietern trifft es nicht unbedingt zu, dass der Benutzer nur über eine einzige E-Mail-Adresse verfügt. Ein Benutzer kann über eine separate E-Mail-Adresse für jeden installierten Transportanbieter oder eine andere Adresse für jede Sitzung eines einzelnen Anbieters verfügen.
    
Weitere Informationen zum Speichern von Anmeldeinformationen in Profilabschnitten finden Sie unter [Nachrichtendienste und Profile](message-services-and-profiles.md) und [IProfSect : IMAPIProp](iprofsectimapiprop.md).
  

