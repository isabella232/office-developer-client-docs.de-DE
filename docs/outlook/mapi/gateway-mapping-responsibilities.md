---
title: Aufgaben bei der Gateway-Zuordnung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0611cb7bfd703097f1c168caa4f743f6770971d0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580216"
---
# <a name="gateway-mapping-responsibilities"></a>Aufgaben bei der Gateway-Zuordnung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein MAPI-fähiges Gateway eine Nachricht mit benannten Eigenschaften in einem der speziellen Eigenschaftensätze empfängt, die für die Verwendung von gatewayzuordnungsfähigen Eigenschaften vorgesehen sind, sollte das Gateway alle Eigenschaften dem Protokoll des Zielmessagingsystems zuordnen. Obwohl mapi empfiehlt, dass Gateways alle benannten Eigenschaften in den speziellen Eigenschaftensätzen behandeln, wird erwartet, dass Gateways nur zwei verarbeiten: E-Mail-Adresse und Adresstyp. Da sich die Eigenschaften E-Mail-Adresse und Adresstyp direkt auf die Nachrichtenübertragung auswirken, ist es wichtig, dass Gateways die Zuordnung dieser beiden Eigenschaften unterstützen. Da Suchschlüssel aus dem Adresstyp und der Adresse eines Benutzers bestehen, sollten sie nach Möglichkeit auch übersetzt werden.
  
Es wird nicht erwartet, dass Eintragsbezeichner häufig behandelt werden. Um die Zuordnung eines Eintragsbezeichners aus einem Messagingsystem zu einem Eintragsbezeichner zu aktivieren, der von einem anderen Messagingsystem verwendet werden kann, muss das Gateway in der Lage sein, das Format beider Systeme zu verwenden. Da die meisten Gateways die Formate von Eintragsbezeichnern nicht kennen, ist die Übersetzung von Eintragsbezeichnern selten.
  
Eine weitere zuordbare Eigenschaft, die nicht häufig übersetzt werden soll, ist der Anzeigename. Gateways sollten Anzeigenamen speichern und übertragen, aber nicht unbedingt übersetzen. 
  

