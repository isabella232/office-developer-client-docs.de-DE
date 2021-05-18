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
  
Wenn ein MAPI-fähiges Gateway eine Nachricht empfängt, die benannte Eigenschaften in einem der speziellen Eigenschaftensätze enthält, die gatewaymappbare Eigenschaften enthalten sollen, sollte das Gateway alle Eigenschaften dem Protokoll des Zielnachrichtensystems zuordnungen. Obwohl MAPI empfiehlt, dass Gateways alle benannten Eigenschaften in den speziellen Eigenschaftensätzen behandeln, werden gateways voraussichtlich nur zwei behandeln: E-Mail-Adresse und Adresstyp. Da sich die Eigenschaften E-Mail-Adresse und Adresstyp direkt auf die Nachrichtenübermittlung auswirken, ist es wichtig, dass Gateways die Zuordnung dieser beiden Eigenschaften unterstützen. Da Suchschlüssel aus dem Adresstyp und der Adresse eines Benutzers bestehen, sollten sie nach Möglichkeit auch übersetzt werden.
  
Es wird nicht erwartet, dass Eintragsbezeichner häufig verarbeitet werden. Zum Aktivieren der Zuordnung eines Eintragsbezeichners, der aus einem Messagingsystem stammt, zu einer Eintrags-ID, die von einem anderen Messagingsystem verwendet werden kann, muss das Gateway das Format beider Systeme verwenden können. Da die meisten Gateways keine Eingabebezeichnerformate kennen, ist die Übersetzung von Eintragsbezeichnern selten.
  
Eine weitere mappable Eigenschaft, die nicht häufig übersetzt werden soll, ist der Anzeigename. Gateways sollten Anzeigenamen speichern und übertragen, aber nicht unbedingt übersetzen. 
  

