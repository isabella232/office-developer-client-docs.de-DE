---
title: Zum Gateway zuzuordnende Eigenschaften
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430476"
---
# <a name="gateway-mappable-properties"></a>Zum Gateway zuzuordnende Eigenschaften

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gateway-zuzuordnende-Eigenschaften sind Eigenschaften, die beim Senden von einer Messaging Domäne an eine andere Übersetzung erfordern. Die MAPI-zuzuordnende-Eigenschaften ermöglichen es, dass Nachrichten Informationen enthält, die ein Gateway erfordern, um sicherzustellen, dass das Ziel Messagingsystem Sie ordnungsgemäß verwendet. Obwohl Gateway-Entwickler diese Übersetzungsfunktion nicht bereitstellen müssen, sollten Sie die zuzuordnende-Eigenschaften als Gelegenheit zur Verbesserung der Verarbeitung von Nachrichteninhalten berücksichtigen.
  
MAPI gibt fünf Typen von Gateway-zuzuordnende-Eigenschaften an:
  
- Distinguished Name (DN)
    
- Anzeigename
    
- E-Mail-Typ
    
- Eintrags-ID
    
- Suchschlüssel
    
Hierbei handelt es sich um den Satz von Adressierungs Eigenschaften, die Empfängern, Absendern, Berichts Empfängern und Delegierten Absendern und Empfängern zugeordnet sind. Um dem Client zu helfen, diese Eigenschaften so zu definieren, dass er Sie speziell behandelt, gibt MAPI eine Benennungskonvention mit benannten Eigenschaften und Eigenschaftensätzen an. Es sind fünf Eigenschaftensätze vorhanden, die benannte Eigenschaften enthalten, die Adressierungs Eigenschaften, die zugeordnet werden müssen. Für jeden zuzuordnende-Eigenschafts ist ein Eigenschaftensatz vorhanden. Die Eigenschaftensätze, in denen diese benannten Adressierungs Einstellungen gespeichert werden, lauten wie folgt.
  
|**Eigenschaftensatz**|**Beschreibung**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Enthält Zeichenfolgeneigenschaften, die als Anzeigenamen verwendet werden.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Enthält Zeichenfolgeneigenschaften, die als e-Mail-Adressen verwendet werden.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Enthält Zeichenfolgeneigenschaften, die als e-Mail-Adresstypen verwendet werden.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Enthält binäre Eigenschaften, die als langfristige Eintragsbezeichner verwendet werden.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Enthält binäre Eigenschaften, die als Suchschlüssel verwendet werden.  <br/> |
   

