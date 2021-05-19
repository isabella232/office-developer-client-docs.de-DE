---
title: Implementieren von Sicherheit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417287"
---
# <a name="implementing-security"></a>Implementieren von Sicherheit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn das Messagingsystem dies erfordert, ist der Transportanbieter für die Implementierung eines geeigneten Sicherheitsniveaus für den Zugriff auf das Messagingsystem verantwortlich. Jede eingehende oder ausgehende Nachricht, die über einen Transportanbieter vom MAPI-Spooler gesendet wird, wird im Kontext einer Anbieteranmeldesitzung behandelt. Der Transportanbieter kann dem Benutzer ein Anmeldedialogfeld anzeigen, in dem die Anmeldeinformationen eines Benutzers angezeigt werden, bevor eine solche Verbindung erstellt wird. Alternativ kann der Transportanbieter die zuvor eingegebenen Anmeldeinformationen des Benutzers im Bereich sicherer Eigenschaften in einem Profilabschnitt speichern und ohne Aufforderung für den Zugriff verwenden.
  
Berücksichtigen Sie bei der Implementierung der Sicherheit Ihres Transportanbieters Folgendes:
  
- Bei mehreren installierten Dienstanbietern können eine Vielzahl von Namen und Kennwörtern einem Benutzer zugeordnet sein.
    
- MAPI ermöglicht mehrere Sitzungen mit mehreren Identitäten. Anbieter werden aufgefordert, mehrere Sitzungen zu unterstützen, müssen dies jedoch nicht tun.
    
- Jede Sitzung mit einem Transportanbieter wird von MAPI einem separaten Abschnitt im Benutzerprofil zugeordnet. Der Transportanbieter kann die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) verwenden, um Zugriff auf diesen Abschnitt zu erhalten, der zum Speichern aller informationen verwendet werden kann, die dieser Sitzung zugeordnet sind, einschließlich Anmeldeinformationen. 
    
- Bei mehreren installierten Transportanbietern stimmt es nicht unbedingt, dass der Benutzer nur über eine einzelne E-Mail-Adresse verfügt. Ein Benutzer kann eine separate E-Mail-Adresse für jeden installierten Transportanbieter oder eine andere Adresse für jede Sitzung eines einzelnen Anbieters haben.
    
Weitere Informationen zum Speichern von Anmeldeinformationen in Profilabschnitten finden Sie unter [Message Services and Profiles](message-services-and-profiles.md) und [IProfSect : IMAPIProp](iprofsectimapiprop.md).
  

