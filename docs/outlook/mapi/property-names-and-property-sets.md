---
title: Eigenschaftennamen und Eigenschaftensätze
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
# <a name="property-names-and-property-sets"></a>Eigenschaftennamen und Eigenschaftensätze

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Name jeder benannten Eigenschaft besteht aus zwei Teilen:
  
- Ein global eindeutiger Bezeichner oder eine GUID, die einen Eigenschaftensatz angibt.
    
- Eine Unicode-Zeichenfolge oder ein 32-Bit-numerischer Wert. 
    
Namen benannter Eigenschaften werden mit einer [MAPINAMEID](mapinameid.md) -Struktur beschrieben. Diese Struktur enthält einen Eigenschaftssatz Member, einen Member zum Angeben des Namens im numerischen oder im Zeichenfolgenformat und ein Element zur Identifizierung des verwendeten Formats. Da der Eigenschaftensatz Teil des Eigenschaftennamens ist, ist er nicht optional. MAPI hat mehrere Eigenschaftssätze für die Verwendung durch Clients und Dienstanbieter definiert, aber wenn ein vorhandener Eigenschaftensatz unangemessen ist, kann ein neuer Eigenschaftssatz definiert werden. Clients und Dienstanbieter können eigene Eigenschaftensätze definieren, indem Sie die [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) -Funktion aufrufen. In der Regel werden diese Eigenschaftensätze für benutzerdefinierte Clientanwendungen erstellt. 
  
MAPI-Eigenschaftensätze werden durch die folgenden Konstanten dargestellt:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
Der PS_MAPI-Eigenschaftensatz ist reserviert; Sie wird von Dienstanbietern verwendet, um Namen für Eigenschaften mit Bezeichnern unterhalb des benannten Eigenschaftenbereichs zu generieren. Der PS_PUBLIC_STRINGS-Eigenschaftensatz wird von Clients für benannte Eigenschaften von IPM-Nachrichten verwendet. Da benannte Eigenschaften im PS_PUBLIC_STRINGS-Eigenschaftensatz auf der Benutzeroberfläche eines Clients angezeigt werden, sollten nicht sichtbare Nachrichten wie die, die zur IPC-Nachrichtenklasse gehören, die Erstellung benannter Eigenschaften mit dieser Eigenschaftsgruppe vermeiden. Stattdessen sollten Sie Eigenschaften im Nachrichtenklassen spezifischen Range-0x6800 bis 0x7FFF erstellen.
  
In der anderen Eigenschaft werden benannte Eigenschaften festgehalten, die Empfänger beschreiben, die normalerweise Mitglieder einer Routingliste sind. Mit demselben Informationstyp wie die Eigenschaften, die den Eigenschaften der Empfängerliste zugeordnet sind, werden die Eigenschaften in diesen Eigenschaftensätzen von Gateways verstanden, um eine Zuordnung für ein Ziel Messagingsystem zu erfordern. Da es fünf Arten von Informationen zur Beschreibung von Eigenschaften gibt, hat MAPI fünf verschiedene Eigenschaftssätze definiert. Ein Client, der eine Nachricht sendet, die einen Adress-und Adresstyp für seine Routing Listenmitglieder enthält, weist für jedes Element in den PS_ROUTING_EMAIL_ADDRESSES-und PS_ROUTING_ADDRTYPE-Eigenschaftssätzen eine benannte Eigenschaft zu. Dadurch wird sichergestellt, dass der Adress-und Adresstyp beim Senden an ein fremdes Messagingsystem weiterhin tragfähig ist.
  
## <a name="see-also"></a>Siehe auch



[Benannte Eigenschaften MAPI](mapi-named-properties.md)

