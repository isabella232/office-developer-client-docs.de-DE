---
title: Entwickeln eines MAPI-Adressbuchanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b1caebdf75d6b7b7d84e786585199f2e780caa05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592501"
---
# <a name="developing-a-mapi-address-book-provider"></a>Entwickeln eines MAPI-Adressbuchanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Adressbuchanbieter stellt Empfängerinformationen an Clientanwendungen, an Nachrichtenspeicher- und Transportanbieter sowie an die MAPI bereit. Empfängerinformationen sind hierarchisch in Speicherdepots organisiert, die als Container bezeichnet werden. Jedes Adressbuch im Profil trägt einen oder mehrere Container der obersten Ebene oder übergeordneten Elemente zum MAPI-Adressbuch bei, einer integrierten Ansicht der Empfängerinformationen von allen Adressbuchanbietern in einer Sitzung. Über das MAPI-Adressbuch erhalten Clients und andere Dienstanbieter Zugriff auf die Daten eines Adressbuchanbieters.
  
MAPI erstellt das integrierte Adressbuch wie folgt:
  
1. Abrufen der Container auf oberster Ebene von jedem Adressbuchanbieter.
    
2. Abrufen der Hierarchietabelle jedes Containers. 
    
3. Kopieren jeder Hierarchietabelle in eine integrierte Hierarchietabelle. Es ist die integrierte Hierarchietabelle, die für den Client verfügbar gemacht wird. 
    
MAPI stellt nur wenige Anforderungen an Adressbuchanbieterautoren. Die Palette möglicher Features, die Sie als Adressbuchautor implementieren können, ist aundreich und flexibel. Beispielsweise kann Ihr Anbieter auf die Bereitstellung einer schreibgeschützten Ansicht eines bestimmten Empfängerinformationstyps oder die Implementierung eines vollständigen Satzes von Features beschränkt sein, sodass Clients oder Anbieter möglicherweise Ergänzungen oder Änderungen an den Empfängerdaten vornehmen und Suchkriterien zum Definieren benutzerdefinierter Ansichten festlegen können. 
  
Die Daten Ihres Anbieters können sich lokal in einer Datei oder Datenbank oder auf einem Remoteserver befinden. Einige Adressbuchanbieter sollten mit einem bestimmten Messagingsystem arbeiten, das eng mit einem Transportanbieter gekoppelt ist, während andere mit jedem Beliebigen Messagingsystem arbeiten können.
  
MAPI definiert einen speziellen Adressbuchanbietertyp, der als persönliches Adressbuch (PAB) bezeichnet wird und einen einzelnen modifizierbaren Container implementiert und Empfängerinformationen, die aus anderen Containern kopiert wurden, sowie direkt erstellte Informationen enthalten kann. Obwohl ein Adressbuchanbieter ein PAB implementieren kann und mehrere PABs zu einem Profil hinzugefügt werden können, kann nur einer dieser Anbieter für die Verwendung als PAB während einer Sitzung festgelegt werden. 
  

