---
title: Sämtliche Gateway-Eigenschaften
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b637f4921165d70ddeda914b4299c35aabe8218f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791767"
---
# <a name="gateway-mappable-properties"></a>Sämtliche Gateway-Eigenschaften

**Betrifft**: Outlook 
  
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
   

