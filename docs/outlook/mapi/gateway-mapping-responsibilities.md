---
title: Aufgaben bei der Gateway-Zuordnung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422754"
---
# <a name="gateway-mapping-responsibilities"></a>Aufgaben bei der Gateway-Zuordnung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein MAPI-fähiges Gateway eine Nachricht mit benannten Eigenschaften in einem der speziellen Eigenschaftssätze empfängt, die zuzuordnende-Eigenschaften enthalten, sollte das Gateway alle Eigenschaften dem Protokoll des Zielmessagingsystems zuordnen. Obgleich MAPI empfiehlt, dass Gateways alle benannten Eigenschaften in den speziellen Eigenschaftssätzen behandeln, wird davon ausgegangen, dass Gateways nur zwei behandeln: e-Mail-Adresse und Adresstyp. Da sich die Eigenschaften von e-Mail-Adresse und Adresstyp direkt auf die Nachrichtenübertragung auswirken, ist es wichtig, dass Gateways die Zuordnung dieser beiden Eigenschaften unterstützen. Da Suchschlüssel den Adresstyp und die Adresse eines Benutzers enthalten, sollten Sie auch übersetzt werden, falls dies möglich ist.
  
Eintragsbezeichner werden nicht häufig behandelt. Um die Zuordnung eines Eintrags Bezeichners, der sich in einem Messagingsystem ausgibt, zu einer Eintrags-ID zu ermöglichen, die von einem anderen Messagingsystem verwendet werden kann, muss das Gateway in der Lage sein, das Format beider Systeme zu verwenden. Da die meisten Gateways die Eingabe-ID-Formate nicht erkennen, ist die Übersetzung von Eintrags Bezeichnern selten.
  
Eine weitere zuzuordnende-Eigenschaft, die nicht häufig übersetzt werden sollte, ist der Anzeigename. Gateways sollten Anzeige Namen speichern und übertragen, aber nicht notwendigerweise übersetzen. 
  

