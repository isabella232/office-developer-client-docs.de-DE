---
title: Entwickeln eines MAPI-Adressbuch Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316702"
---
# <a name="developing-a-mapi-address-book-provider"></a>Entwickeln eines MAPI-Adressbuch Anbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Adressbuchanbieter liefert Empfängerinformationen für Clientanwendungen, für Nachrichtenspeicher-und Transportanbieter sowie für MAPI. Empfängerinformationen werden hierarchisch in Speicher Fächern, die als Container bezeichnet werden, organisiert. Jedes Adressbuch im Profil trägt einen oder mehrere Container der obersten Ebene oder eines übergeordneten Elements zum MAPI-Adressbuch bei, eine integrierte Ansicht von Empfängerinformationen aller Adressbuchanbieter in einer Sitzung. Über das MAPI-Adressbuch erhalten Clients und andere Dienstanbieter Zugriff auf die Daten eines Adressbuch Anbieters.
  
MAPI erstellt das integrierte Adressbuch nach folgendem:
  
1. Abrufen der Container der obersten Ebene aus jedem Adressbuchanbieter.
    
2. Abrufen der Hierarchietabelle der einzelnen Container. 
    
3. Kopieren jeder Hierarchietabelle in eine integrierte Hierarchietabelle. Es ist die integrierte Hierarchietabelle, die für den Client verfügbar gemacht wird. 
    
MAPI stellt wenige Anforderungen an Writer für Adressbuchanbieter. Die Möglichkeiten, die Sie als Adressbuch Autor implementieren können, sind vielfältig und flexibel. Beispielsweise könnte Ihr Anbieter auf die Bereitstellung einer schreibgeschützten Ansicht eines bestimmten Typs von Empfängerinformationen beschränken oder einen vollständigen Satz von Features implementieren, sodass Clients oder Anbieter möglicherweise Ergänzungen oder Änderungen an den Empfängerdaten vornehmen und Suchkriterien für die Definition angepasster Ansichten. 
  
Die Daten Ihres Anbieters können sich lokal in einer Datei oder Datenbank oder auf einem Remoteserver befinden. Einige Adressbuchanbieter sollen mit einem bestimmten Messagingsystem zusammenarbeiten, eng mit einem Transportanbieter gekoppelt, während andere mit einem beliebigen Messagingsystem arbeiten können.
  
MAPI definiert einen speziellen Adressbuchanbieter, der als persönliches Adressbuch bezeichnet wird, oder ein PAB, das einen einzelnen änderbaren Container implementiert und Empfängerinformationen aus anderen Containern sowie direkt erstellte Informationen enthalten kann. Auch wenn ein Adressbuchanbieter ein PAB implementieren kann und mehrere PABs zu einem Profil hinzugefügt werden können, kann nur einer dieser Anbieter als PAB während einer Sitzung festgelegt werden. 
  

