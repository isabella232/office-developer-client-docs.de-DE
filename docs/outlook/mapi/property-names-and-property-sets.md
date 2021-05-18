---
title: Eigenschaftsnamen und Eigenschaftensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328546"
---
# <a name="property-names-and-property-sets"></a>Eigenschaftsnamen und Eigenschaftensätze

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Name jeder benannten Eigenschaft hat zwei Teile:
  
- Eine global eindeutige ID oder GUID, die einen Eigenschaftensatz angibt.
    
- Eine Unicode-Zeichenzeichenfolge oder ein numerischer 32-Bit-Wert. 
    
Namen benannter Eigenschaften werden mithilfe einer [MAPINAMEID-Struktur](mapinameid.md) beschrieben. Diese Struktur enthält ein Element des Eigenschaftensatzs, ein Element zum Angeben des Namens im Numerischen oder Zeichenfolgenformat und ein Element zum Identifizieren des verwendeten Formats. Da der Eigenschaftensatz Teil des Namens der Eigenschaft ist, ist er nicht optional. MAPI hat mehrere Eigenschaftssätze für die Verwendung durch Clients und Dienstanbieter definiert, aber wenn ein vorhandener Eigenschaftensatz nicht geeignet ist, kann ein neuer Eigenschaftensatz definiert werden. Clients und Dienstanbieter können ihre eigenen Eigenschaftensätze definieren, indem sie [die CoCreateGUID-Funktion](https://msdn.microsoft.com/library/ms688568.aspx) aufrufen. In der Regel werden diese Eigenschaftssätze für benutzerdefinierte Clientanwendungen erstellt. 
  
Die Eigenschaftssätze von MAPI werden durch die folgenden Konstanten dargestellt:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
Der PS_MAPI-Eigenschaftssatz ist reserviert. Es wird von Dienstanbietern verwendet, um Namen für Eigenschaften mit Bezeichnern unterhalb des benannten Eigenschaftenbereichs zu generieren. Der PS_PUBLIC_STRINGS wird von Clients für benannte Eigenschaften von IPM-Nachrichten verwendet. Da benannte Eigenschaften im PS_PUBLIC_STRINGS-Eigenschaftssatz auf der Benutzeroberfläche eines Clients angezeigt werden, sollten nicht lesbare Nachrichten, z. B. solche, die zur IPC-Nachrichtenklasse gehören, vermeiden, benannte Eigenschaften mit diesem Eigenschaftensatz zu erstellen. Stattdessen sollten sie Eigenschaften im nachrichtenklassenspezifischen Bereich erstellen, 0x6800 bis 0x7FFF.
  
Die anderen Eigenschaftensätze enthalten benannte Eigenschaften, die Empfänger beschreiben, die in der Regel Mitglieder einer Routingliste sind. Mit demselben Informationstyp wie die Eigenschaften, die Empfängerlisteneigenschaften zugeordnet sind, werden Eigenschaften in diesen Eigenschaftensätzen von Gateways verstanden, um eine Zuordnung für ein Zielnachrichtensystem zu erfordern. Da es fünf Arten von Informationen zum Beschreiben von Eigenschaften gibt, hat MAPI fünf verschiedene Eigenschaftensätze definiert. Ein Client, der eine Nachricht sendet, die eine Adresse und einen Adresstyp für seine Routinglistenmitglieder enthalten muss, weist jedem Element in den Eigenschaftensätzen PS_ROUTING_EMAIL_ADDRESSES und PS_ROUTING_ADDRTYPE eine benannte Eigenschaft zu. Dadurch wird sichergestellt, dass die Adresse und der Adresstyp beim Senden an ein fremdes Messagingsystem weiterhin praktikabel sind.
  
## <a name="see-also"></a>Siehe auch



[Benannte Eigenschaften MAPI](mapi-named-properties.md)

