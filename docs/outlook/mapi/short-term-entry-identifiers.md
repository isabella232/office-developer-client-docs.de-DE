---
title: Kurzfristige Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29dcc79d644ba4a5bf46f06bd8c6466e854ac890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598983"
---
# <a name="short-term-entry-identifiers"></a>Kurzfristige Eintragsbezeichner

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein kurzfristiger Eintragsbezeichner wird von einem Dienstanbieter einem Objekt zugewiesen, wenn der Bezeichner schnell erstellt werden muss und nicht über einen zeitraum- oder entfernungsbezogenen Zeitraum bestehen muss. Die Eindeutigkeit eines kurzfristigen Eintragsbezeichners wird nur über die Dauer der aktuellen Sitzung auf der aktuellen Arbeitsstation garantiert. In der Regel ist ein kurzfristiger Eintragsbezeichner nur gültig, bis das objekt, das es darstellt, freigegeben wird. 
  
Kurzfristige Eintragsbezeichner werden Zeilen in Tabellen und Einträgen in Dialogfeldern zugewiesen, in denen daten schnell zum Durchsuchen bereitgestellt werden müssen. Beispielsweise weisen Nachrichtenspeicheranbieter Zeilen von Nachrichten in einem Inhaltsverzeichnis und Empfängern in einer Empfängertabelle kurzfristige Eintragsbezeichner zu. 

Clients können diese kurzfristigen Eintragsbezeichner verwenden, um die durch die Tabellenzeilen dargestellten Objekte zu öffnen. Im Gegensatz zu langfristigen Eintragsbezeichnern, die mit einer der **OpenEntry-Methoden** verwendet werden können, sollten kurzfristige Eintragsbezeichner jedoch mit der **OpenEntry-Methode** des Containers verwendet werden. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implementieren kurzfristiger Eintragsbezeichner

Die gängigsten Methoden zum Implementieren von kurzfristigen Eintragsbezeichnern sind:
  
- Die kurzfristigen Eintragsbezeichner werden mit den langfristigen Bezeichnern identisch, sodass alle Flags nicht festgelegt werden. 
    
- Unterscheiden Sie sich die Bezeichner für den kurzfristigen Eintrag von den langfristigen Bezeichnern, indem Sie alle Flags festlegen. 
    
Clients können einen kurzfristigen Eintragsbezeichner des zweiten Typs identifizieren, indem sie das **abFlags-Element** wie folgt untersuchen: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Einige Dienstanbieter löschen ein oder mehrere Flags, um kurzfristige Eintragsbezeichner mit höherer Gültigkeit zu erstellen. Die folgenden **abFlags-Mitglieder** stellen beispielsweise kurzfristige Eintragsbezeichner dar, die für mehrere Tage oder für mehrere Sitzungen verwendet werden können: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Clients erwerben, verwenden und verwerfen schnell kurzfristige Eintragsbezeichner. In den meisten Fällen können sie auf die gleiche Weise wie langfristige Eintragsbezeichner verwendet werden. Sie können aus einer Tabelle abgerufen, an die **OpenEntry-Methode** übergeben und mit der **CompareEntryIDs-Methode** verglichen werden. Die einzige Ausnahme besteht darin, dass sie nie von der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) zurückgegeben werden. Die von **GetProps zurückgegebenen** Eigenschaften sind immer langfristige Eintragsbezeichner. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

