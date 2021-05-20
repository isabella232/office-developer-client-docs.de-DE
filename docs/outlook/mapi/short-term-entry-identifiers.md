---
title: Kurzfristige Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439562"
---
# <a name="short-term-entry-identifiers"></a>Kurzfristige Eintragsbezeichner

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein kurzfristiger Eintragsbezeichner wird von einem Dienstanbieter einem Objekt zugewiesen, wenn der Bezeichner schnell erstellt werden muss und nicht über zeit- oder entfernungsüber einen Bestimmten Zeitraum verfügen muss. Die Eindeutigkeit eines kurzfristigen Eintragsbezeichners wird nur während der Laufzeit der aktuellen Sitzung auf der aktuellen Arbeitsstation garantiert. In der Regel ist eine kurzfristige Eintrags-ID nur gültig, bis das objekt, das sie darstellt, freigegeben wird. 
  
Kurzfristige Eintragsbezeichner werden Zeilen in Tabellen und Einträgen in Dialogfeldern zugewiesen, wo es erforderlich ist, schnell Daten für das Browsen zur Verfügung zu stellen. Nachrichtenspeicheranbieter weisen beispielsweise Zeilen von Nachrichten in einer Inhaltstabelle und Empfängern in einer Empfängertabelle kurzfristige Eintragsbezeichner zu. 

Clients können diese kurzfristigen Eintragsbezeichner verwenden, um die durch die Tabellenzeilen dargestellten Objekte zu öffnen. Im Gegensatz zu langfristigen Eintragsbezeichnern, die mit einer der **OpenEntry-Methoden** verwendet werden können, sollten jedoch kurzfristige Eintragsbezeichner mit der **OpenEntry-Methode** des Containers verwendet werden. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implementieren kurzfristiger Eintragsbezeichner

Die gängigsten Methoden zum Implementieren kurzfristiger Eintragsbezeichner sind:
  
- Machen Sie die kurzfristigen Eintragsbezeichner mit den langfristigen Bezeichnern identisch, ohne dass alle Kennzeichen nicht mehr verwendet werden. 
    
- Ändern Sie die Kurzzeiteintragsbezeichner von den langfristigen Bezeichnern, indem Sie alle Kennzeichen festlegen. 
    
Clients können einen kurzfristigen Eintragsbezeichner des zweiten Typs identifizieren, indem sie sein **abFlags-Mitglied** wie folgt untersuchen: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Einige Dienstanbieter löschen ein oder mehrere Kennzeichen, um kurzfristige Eintragsbezeichner zu erstellen, die eine höhere Gültigkeit haben. Die folgenden **abFlags-Mitglieder** stellen beispielsweise kurzfristige Eintragsbezeichner dar, die für mehrere Tage oder für mehrere Sitzungen verwendet werden können: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Clients erwerben, verwenden und verwerfen schnell kurzfristige Eintragsbezeichner. Sie können meist auf die gleiche Weise wie langfristige Eintragsbezeichner verwendet werden. Sie können aus einer Tabelle abgerufen, an die **OpenEntry-Methode** übergeben und mit der **CompareEntryIDs-Methode verglichen** werden. Die einzige Ausnahme ist, dass sie nie von der [IMAPIProp::GetProps-Methode zurückgegeben](imapiprop-getprops.md) werden. Die von **GetProps** zurückgegebenen Eigenschaften sind immer langfristige Eintragsbezeichner. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

