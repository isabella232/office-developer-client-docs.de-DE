---
title: Gateway Zuordnung Zuständigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad5f4e896b748dc0d7495c428af093af57bc7cdd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791768"
---
# <a name="gateway-mapping-responsibilities"></a>Gateway Zuordnung Zuständigkeiten

**Betrifft**: Outlook 
  
Wenn ein MAPI-fähigen Gateway eine Nachricht mit benannten Eigenschaften in einem der die spezielle Eigenschaftensätze festgelegte Gateway sämtliche Eigenschaften enthält empfängt, sollte das Gateway alle Eigenschaften des Protokolls des Ziels Messagingsystem zuordnen. Obwohl MAPI empfiehlt, dass Gateways alle benannte Eigenschaften in die spezielle Eigenschaftensätze zu behandeln, Gateways werden erwartet, dass nur zwei behandeln: e-Mail-Adresse und Adresstyp. Da der e-Mail-Adresse und den Typ Adresseigenschaften direkt die Nachrichtenübermittlung beeinträchtigen, ist es wichtig, Gateways die Zuordnung dieser beiden Eigenschaften unterstützen. Da Search Schlüssel Adresstyp und Adresse eines Benutzers bestehen, sollten sie auch nach Möglichkeit übersetzt werden.
  
Eintragsbezeichner voraussichtlich nicht häufig behandelt werden. Um Zuordnung von Eintrags-ID zu aktivieren, die in einem messaging-System auf einen Eintrag Bezeichner stammt, die von einem anderen Messagingsystem verwendet werden kann, muss das Gateway das Format der beiden Systemen verwenden können. Da die meisten Gateways keine Eintrags-ID Formate kennen, ist die Übersetzung von Eintragsbezeichner selten.
  
Eine andere sämtliche-Eigenschaft, die nicht häufig übersetzt werden erwartet wird, ist der Anzeigename. Gateways sollte Anzeigenamen speichern und senden, aber nicht unbedingt zu übersetzen. 
  

