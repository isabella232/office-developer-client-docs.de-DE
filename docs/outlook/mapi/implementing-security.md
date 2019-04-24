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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310059"
---
# <a name="implementing-security"></a>Implementieren von Sicherheit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn das Messagingsystem dies erfordert, ist der Transportanbieter für die Implementierung einer angemessenen Sicherheitsstufe für den Zugriff auf das Messagingsystem verantwortlich. Jede eingehende oder ausgehende Nachricht, die über den MAPI-Spooler über einen Transportanbieter gesendet wird, wird im Kontext einer Anbieter Anmeldesitzung behandelt. Der Transportanbieter kann dem Benutzer ein Anmeldedialogfeld anzeigen, das die Anmeldeinformationen eines Benutzers anfordert, bevor eine solche Verbindung hergestellt wird. Alternativ kann der Transportanbieter die zuvor eingegebenen Anmeldeinformationen des Benutzers im Secure-Eigenschaftsbereich eines Profil Abschnitts speichern und für den Zugriff ohne Eingabeaufforderungen verwenden.
  
Berücksichtigen Sie beim Implementieren der Sicherheit Ihres Transportanbieters Folgendes:
  
- Bei mehreren installierten Dienstanbietern kann es eine Vielzahl von Namen und Kennwörtern geben, die einem Benutzer zugeordnet sind.
    
- MAPI ermöglicht mehrere Sitzungen mit mehreren Identitäten. Anbieter werden aufgefordert, mehrere Sitzungen zu unterstützen, sind jedoch nicht dazu verpflichtet.
    
- Jede Sitzung mit einem Transportanbieter wird von MAPI mit einem diskreten Abschnitt im Profil des Benutzers verknüpft. Der Transportanbieter kann die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode verwenden, um Zugriff auf diesen Abschnitt zu erhalten, der zum Speichern der dieser Sitzung zugeordneten Informationen, einschließlich der Anmeldeinformationen, verwendet werden kann. 
    
- Bei mehreren installierten Transportanbietern ist es nicht unbedingt wahr, dass der Benutzer nur eine einzige e-Mail-Adresse hat. Ein Benutzer kann eine separate e-Mail-Adresse für jeden installierten Transportanbieter haben oder eine andere Adresse für jede Sitzung in einem einzelnen Anbieter haben.
    
Weitere Informationen zum Speichern von Anmeldeinformationen in Profil Abschnitten finden Sie unter [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect: IMAPIProp](iprofsectimapiprop.md).
  

