---
title: Entwicklung eines MAPI-Adressbuchanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 731ebf6f61db8e9f425d48ab63cb7b81035a41c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584282"
---
# <a name="developing-a-mapi-address-book-provider"></a>Entwicklung eines MAPI-Adressbuchanbieters

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Adressbuch-Dienstanbieter liefert Empfängerinformationen Clientanwendungen Nachrichtenspeicher und transport-Anbieter und MAPI. Empfängerinformationen ist in Storage Kästchen bekannt als Container hierarchisch organisiert. Jedes Adressbuch im Profil trägt eine oder mehr auf oberster Ebene oder übergeordneten Inhaltstyps, Bücher zu MAPI-Adressbuch, eine integrierte Ansicht der Empfängerinformationen aus allen Adresse Container Anbieter in einer Sitzung. Es ist über das MAPI-Adressbuch, dass Clients und andere Telefoniedienstanbieter Zugriff auf die Daten der Adressbuch-Dienstanbieter erhalten.
  
MAPI-builds integrierte Adressbuch nach:
  
1. Abrufen von Container der obersten Ebene aus jeder Adressbuchanbieter.
    
2. Abrufen des Containers Hierarchietabelle. 
    
3. Kopieren jede Hierarchietabelle in eine Hierarchietabelle integrierte. Es ist die integrierte Hierarchietabelle, die an den Client verfügbar gemacht wird. 
    
MAPI erfordert einige Anforderungen auf Address Book Anbieterwriter. Der Bereich der möglichen Features können Sie implementieren, wie ein Address Book Writer verschiedenen und flexible ist. Beispielsweise konnte Ihres Anbieters mit der Bereitstellung einer nur-Lese-Ansicht eines bestimmten Typs von Empfängerinformationen beschränkt werden oder implementieren eine umfassende Auswahl an Features, vielleicht und-Clients oder Anbieter um vorgenommene Hinzufügungen oder Änderungen an den Daten des Empfängers zu gestalten und zugrunde liegen die Suchkriterien Sie für benutzerdefinierte Ansichten definieren. 
  
Daten des Anbieters können lokal in einer Datei oder Datenbank oder auf einem Remoteserver befinden. Einige adressbuchanbietern implementierte sollen arbeiten mit einem bestimmten Messagingsystem eng mit eines Transportdienstes gekoppelt, während andere Benutzer mit messaging-System ausgeführt werden können.
  
MAPI definiert einen speziellen Adressbuchanbieter ein persönliches Adressbuch oder PAB, die einen einzelnen änderbaren Container implementiert und kann halten, kopiert aus anderen Containern sowie Informationen, die direkt erstellt Empfängerinformationen bezeichnet. Zwar alle Adressbuchanbieter ein PAB implementieren kann und mehrere PABs zu einem Profil hinzugefügt werden können, kann nur eine dieser Anbieter als PAB während einer Sitzung ein Betrieb festgelegt werden. 
  

