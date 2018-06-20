---
title: Eigenschaftennamen und Eigenschaftensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c586d70054542e8d20c90a8caceafabbbb408de8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795354"
---
# <a name="property-names-and-property-sets"></a>Eigenschaftennamen und Eigenschaftensätze

  
  
**Betrifft**: Outlook 
  
Der Name jeder benannten Eigenschaft besteht aus zwei Teilen:
  
- Einen global eindeutigen Bezeichner oder um eine GUID, die einen Eigenschaftensatz angibt.
    
- Eine Unicode-Zeichenfolge oder eine 32-Bit-numerischen Wert. 
    
Namen der benannten Eigenschaften werden durch eine [MAPINAMEID](mapinameid.md) Struktur beschrieben. Diese Struktur enthält ein Eigenschaft Set-Element, ein Element zum Angeben des Namens im Format numerischen oder Zeichenfolgenwerten und Mitglied zum Identifizieren, welches Format verwendet wird. Da Eigenschaftensatzes Teil der Name der Eigenschaft ist, ist nicht optional. MAPI hat mehrere Eigenschaftensätze für die Verwendung durch Clients und Dienstanbieter definiert, aber wenn ein vorhandene Eigenschaftensatz nicht geeignet ist, kann ein neuen Eigenschaftensatz definiert werden. Clients und Dienstanbieter können ihre eigenen Eigenschaftensätze definieren, indem [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) -Funktion aufgerufen. In der Regel werden die folgenden Eigenschaftensätze für benutzerdefinierter Clientanwendungen erstellt. 
  
MAPI Eigenschaftensätze werden durch die folgenden Konstanten dargestellt:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
Der Eigenschaftensatz PS_MAPI ist reserviert. Es wird von Dienstanbietern verwendet, um Namen für Eigenschaften mit Bezeichnern unterhalb des Bereichs für die benannte Eigenschaft zu generieren. Die PS_PUBLIC_STRINGS-Eigenschaft festgelegt wird von Clients für benannte Eigenschaften der IPM-Nachrichten verwendet. Da benannte Eigenschaften im Eigenschaftensatz PS_PUBLIC_STRINGS angezeigt in einer Client-Benutzeroberfläche, nicht sichtbare Nachrichten wie erstellen, die die Nachrichtenklasse IPK gehören vermeiden, sollten benannte Eigenschaften diese Eigenschaft festgelegt. In diesem Fall sollten sie Eigenschaften in der Nachricht Klasse-spezifischen Bereich 0x6800 über 0x7FFF erstellen.
  
Die anderen Eigenschaftensätze halten benannten eigenschaftenauflistung Empfänger an, die in der Regel Mitglieder einer Verteilerliste sind. Enthält die gleiche Art von Informationen als die Eigenschaften, die Empfängerliste Eigenschaften zugeordnet sind, werden Eigenschaften in dieser Eigenschaftensätze Gateways verständlich Zuordnung für ein Ziel Messagingsystem erforderlich ist. Da fünf Arten von Informationen für die Beschreibung der Eigenschaften vorhanden sind, hat fünf verschiedenen Eigenschaftensätze MAPI definiert ist. Ein Client sendet, dass eine Nachricht, die eine Adresse und den Adresstyp für Membern Liste routing umfassen muss eine benannte Eigenschaft für jedes Mitglied in der PS_ROUTING_EMAIL_ADDRESSES und PS_ROUTING_ADDRTYPE-Eigenschaft weist festgelegt. Dadurch wird sichergestellt, dass die Adresse und den Adresstyp verwendbar, wenn an einem fremden Messagingsystem gesendet bleiben.
  
## <a name="see-also"></a>Siehe auch



[Benannte Eigenschaften MAPI](mapi-named-properties.md)

