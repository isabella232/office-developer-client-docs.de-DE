---
title: Sämtliche Gateway-Eigenschaften
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 07c215511f010741e69c08c184df0ca3ce461e13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583617"
---
# <a name="gateway-mappable-properties"></a>Sämtliche Gateway-Eigenschaften

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gateway-sämtliche Eigenschaften sind, die Übersetzung beim Senden von einer messaging-Domäne in eine andere erforderlich sind. Zum Zuordnen geeignete Gateway des MAPI-Eigenschaften aktivieren Nachrichten an Informationen enthalten, die ein Gateway aus, um sicherzustellen, dass das Ziel messaging-System verwendet ordnungsgemäß erfordert. Obwohl Entwickler Gateway nicht erforderlich sind, diese Übersetzungsfunktion bereitstellen, sollten sie Gateway sämtliche Eigenschaften als Gelegenheit zur Behandlung von Inhalt zu verbessern.
  
MAPI gibt fünf Typen von Gateways sämtliche Eigenschaften:
  
- Anzeigename
    
- E-Mail-Adresse
    
- E-Mail-Typ
    
- Eintrags-ID
    
- Suchen-Taste
    
Dies ist der Satz von reagieren auf Eigenschaften, die Empfänger, Absender, Berichtempfänger und delegierte Absender und Empfänger zugeordnet sind. Gibt an, mit denen Ihre Client diese Eigenschaften zu definieren, sodass ein Gateway sie speziell behandelt, MAPI eine Benennungskonvention von benannten Eigenschaften und Eigenschaftensätze. Fünf Eigenschaftensätze vorhanden benannte Eigenschaften, die Adressierung Eigenschaften enthalten, die zugeordnet werden müssen. Es gibt eine Eigenschaft für jeden Typ, der sämtliche-Eigenschaft festgelegt. Die Eigenschaftensätze, die diese benannte reagieren auf Eigenschaften enthalten sind wie folgt.
  
|**Eigenschaftensatz**|**Beschreibung**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Enthält Zeichenfolgeneigenschaften als Anzeigenamen verwendet.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Enthält Zeichenfolgeneigenschaften als e-Mail-Adressen verwendet wird.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Enthält Zeichenfolgeneigenschaften als e-Mail-Adresstypen verwendet wird.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Enthält binäre Eigenschaften als langfristige-Eintragsbezeichner verwendet wird.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Binäre Eigenschaften, die als Suche Schlüssel enthält.  <br/> |
   

