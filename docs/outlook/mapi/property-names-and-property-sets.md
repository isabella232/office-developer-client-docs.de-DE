---
title: Eigenschaftennamen und Eigenschaftensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3dafe9fa75dee6f626197d8974c407dec7ad5a90
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586845"
---
# <a name="property-names-and-property-sets"></a>Eigenschaftennamen und Eigenschaftensätze

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Name jeder benannten Eigenschaft besteht aus zwei Teilen:
  
- Ein global eindeutiger Bezeichner oder guid, der einen Eigenschaftensatz angibt.
    
- Eine Unicode-Zeichenfolge oder ein numerischer 32-Bit-Wert. 
    
Namen benannter Eigenschaften werden mithilfe einer [MAPINAMEID-Struktur](mapinameid.md) beschrieben. Diese Struktur enthält ein Eigenschaftensatzelement, ein Element zum Angeben des Namens im numerischen oder Zeichenfolgenformat und ein Element zum Identifizieren des verwendeten Formats. Da der Eigenschaftensatz Teil des Eigenschaftsnamens ist, ist er nicht optional. MAPI hat mehrere Eigenschaftensätze für die Verwendung durch Clients und Dienstanbieter definiert, aber wenn ein vorhandener Eigenschaftensatz unangemessen ist, kann ein neuer Eigenschaftensatz definiert werden. Clients und Dienstanbieter können ihre eigenen Eigenschaftensätze definieren, indem sie die [CoCreateGUID-Funktion](https://msdn.microsoft.com/library/ms688568.aspx) aufrufen. In der Regel werden diese Eigenschaftensätze für benutzerdefinierte Clientanwendungen erstellt. 
  
Die Eigenschaftensätze der MAPI werden durch die folgenden Konstanten dargestellt:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
Der PS_MAPI Eigenschaftensatz ist reserviert. es wird von Dienstanbietern verwendet, um Namen für Eigenschaften mit Bezeichnern unterhalb des benannten Eigenschaftenbereichs zu generieren. Der PS_PUBLIC_STRINGS Eigenschaftensatz wird von Clients für benannte Eigenschaften von IPM-Nachrichten verwendet. Da benannte Eigenschaften im PS_PUBLIC_STRINGS Eigenschaftensatz auf der Benutzeroberfläche eines Clients angezeigt werden, sollten nichtvisierbare Nachrichten wie diejenigen, die zur IPC-Nachrichtenklasse gehören, das Erstellen benannter Eigenschaften mit diesem Eigenschaftensatz vermeiden. Stattdessen sollten sie Eigenschaften im nachrichtenklassenspezifischen Bereich erstellen, 0x6800 über 0x7FFF.
  
Die anderen Eigenschaftensätze enthalten benannte Eigenschaften, die Empfänger beschreiben, die in der Regel Mitglieder einer Routingliste sind. Mit dem gleichen Informationstyp wie die Eigenschaften, die Empfängerlisteneigenschaften zugeordnet sind, werden eigenschaften in diesen Eigenschaftensätzen von Gateways verstanden, um eine Zuordnung für ein Zielmessagingsystem zu erfordern. Da es fünf Arten von Informationen zum Beschreiben von Eigenschaften gibt, hat MAPI fünf verschiedene Eigenschaftensätze definiert. Ein Client, der eine Nachricht sendet, die eine Adresse und einen Adresstyp für seine Routinglistenmember enthalten muss, weist jedem Mitglied in den Eigenschaftensätzen PS_ROUTING_EMAIL_ADDRESSES und PS_ROUTING_ADDRTYPE eine benannte Eigenschaft zu. Dadurch wird sichergestellt, dass die Adresse und der Adresstyp beim Senden an ein Fremdnachrichtensystem funktionsfähig bleiben.
  
## <a name="see-also"></a>Siehe auch



[Benannte Eigenschaften MAPI](mapi-named-properties.md)

