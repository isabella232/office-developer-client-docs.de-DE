---
title: Zum Gateway zuzuordnende Eigenschaften
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7fd8608dbe8d0e848778121204ca04b4529e83e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630831"
---
# <a name="gateway-mappable-properties"></a>Zum Gateway zuzuordnende Eigenschaften

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zuzuordnende Eigenschaften für Gateways sind Eigenschaften, die möglicherweise eine Übersetzung erfordern, wenn sie von einer Messagingdomäne an eine andere gesendet werden. Die gatewayzuordnungsfähigen Eigenschaften der MAPI ermöglichen es Nachrichten, Informationen einzuschließen, die ein Gateway erfordern, um sicherzustellen, dass das Zielmessagingsystem es ordnungsgemäß verwendet. Obwohl Gatewayentwickler diese Übersetzungsfunktion nicht bereitstellen müssen, sollten sie gatewayzuordnungsfähige Eigenschaften als Gelegenheit betrachten, die Behandlung von Nachrichteninhalten zu verbessern.
  
MAPI gibt fünf Typen von gatewayzuordnungsfähigen Eigenschaften an:
  
- Distinguished Name (DN)
    
- Anzeigename
    
- E-Mail-Typ
    
- Eintragsbezeichner
    
- Suchschlüssel
    
Dies ist der Satz von Adressierungseigenschaften, die Empfängern, Absendern, Berichtsempfängern und delegierten Absendern und Empfängern zugeordnet sind. Um dem Client zu helfen, diese Eigenschaften so zu definieren, dass sie von einem Gateway speziell behandelt werden, gibt MAPI eine Benennungskonvention mithilfe benannter Eigenschaften und Eigenschaftensätze an. Es sind fünf Eigenschaftensätze vorhanden, die benannte Eigenschaften enthalten, die Adressierungseigenschaften, die zugeordnet werden müssen. Für jeden Typ der zuordbaren Eigenschaft ist ein Eigenschaftensatz festgelegt. Die Eigenschaftensätze, die diese benannten Adressierungseigenschaften enthalten, sind wie folgt.
  
|**Eigenschaftensatz**|**Beschreibung**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Enthält Zeichenfolgeneigenschaften, die als Anzeigenamen verwendet werden.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Enthält Zeichenfolgeneigenschaften, die als E-Mail-Adressen verwendet werden.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Enthält Zeichenfolgeneigenschaften, die als E-Mail-Adresstypen verwendet werden.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Enthält binäre Eigenschaften, die als langfristige Eintragsbezeichner verwendet werden.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Enthält binäre Eigenschaften, die als Suchschlüssel verwendet werden.  <br/> |
   

