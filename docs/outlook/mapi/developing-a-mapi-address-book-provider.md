---
title: Entwickeln eines MAPI-Adressbuchanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409370"
---
# <a name="developing-a-mapi-address-book-provider"></a>Entwickeln eines MAPI-Adressbuchanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Adressbuchanbieter stellt Empfängerinformationen für Clientanwendungen, für Nachrichtenspeicher- und Transportanbieter sowie für MAPI zur Verfügung. Empfängerinformationen sind hierarchisch in Speicherfächern organisiert, die als Container bezeichnet werden. Jedes Adressbuch im Profil trägt einen oder mehrere übergeordnete Container der obersten Ebene zum MAPI-Adressbuch bei, eine integrierte Ansicht von Empfängerinformationen von allen Adressbuchanbietern in einer Sitzung. Über das MAPI-Adressbuch erhalten Clients und andere Dienstanbieter Zugriff auf die Daten eines Adressbuchanbieters.
  
MAPI erstellt das integrierte Adressbuch durch:
  
1. Abrufen der Container auf oberster Ebene von jedem Adressbuchanbieter.
    
2. Abrufen der Hierarchietabelle jedes Containers. 
    
3. Kopieren jeder Hierarchietabelle in eine integrierte Hierarchietabelle. Es ist die integrierte Hierarchietabelle, die für den Client verfügbar gemacht wird. 
    
MapI stellt nur wenige Anforderungen für Adressbuchanbieterautoren. Die Palette der möglichen Features, die Sie als Adressbuchautor implementieren können, ist vielfältig und flexibel. Ihr Anbieter kann beispielsweise auf die Bereitstellung einer schreibgeschützten Ansicht einer bestimmten Art von Empfängerinformationen oder die Implementierung eines vollständigen Features beschränkt sein, sodass Clients oder Anbieter möglicherweise Ergänzungen oder Änderungen an den Empfängerdaten und Suchkriterien zum Definieren angepasster Ansichten festlegen können. 
  
Die Daten Ihres Anbieters können sich lokal in einer Datei oder Datenbank oder auf einem Remoteserver befinden. Einige Adressbuchanbieter sind für die Zusammenarbeit mit einem bestimmten Messagingsystem gedacht, das eng mit einem Transportanbieter gekoppelt ist, während andere mit einem beliebigen Messagingsystem arbeiten können.
  
MAPI definiert einen speziellen Typ von Adressbuchanbietern, das als persönliches Adressbuch oder PAB bezeichnet wird, das einen einzelnen veränderbaren Container implementiert und Empfängerinformationen, die aus anderen Containern kopiert wurden, sowie direkt erstellte Informationen enthalten kann. Obwohl jeder Adressbuchanbieter ein PAB implementieren kann und einem Profil mehrere PABs hinzugefügt werden können, kann nur einer dieser Anbieter während einer sitzung als PAB bezeichnet werden. 
  

