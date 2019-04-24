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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339193"
---
# <a name="short-term-entry-identifiers"></a>Kurzfristige Eintragsbezeichner

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine kurzfristige Eintrags-ID wird einem Objekt von einem Dienstanbieter zugewiesen, wenn der Bezeichner schnell erstellt werden muss und nicht über die Zeit oder den Abstand zu halten ist. Die Eindeutigkeit einer kurzfristigen Eintrags-ID wird nur über die Lebensdauer der aktuellen Sitzung auf der aktuellen Arbeitsstation gewährleistet. NormalerWeise ist eine kurzfristige Eintrags-ID nur gültig, bis das Objekt, das es darstellt, freigegeben wird. 
  
Kurzfristige Eintrags-IDs werden Zeilen in Tabellen und Einträgen in Dialogfeldern zugewiesen, in denen Daten schnell zum Browsen bereitgestellt werden müssen. Beispielsweise weisen Nachrichtenspeicher Anbieter kurzfristige Eintragsbezeichner zu Zeilen von Nachrichten in einer Inhaltstabelle und Empfängern in einer Recipients-Tabelle zu. 

Clients können diese kurzfristigen Eintragsbezeichner verwenden, um die Objekte zu öffnen, die von den Tabellenzeilen dargestellt werden. Im Gegensatz zu langfristigen Eintrags Bezeichnern, die mit einer der openEntry **** -Methoden verwendet werden können, sollten jedoch kurzfristige Eintragsbezeichner mit der OpenEntry-Methode des Containers verwendet werden. **** 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implementieren von kurzfristigen Eintrags Bezeichnern

Die gängigsten Methoden zum Implementieren von kurzfristigen Eintrags-IDs sind folgende:
  
- Festlegen, dass die kurzfristigen Eintragsbezeichner mit den langfristigen Bezeichnern identisch sind, sodass alle Flags nicht mehr verfügbar sind. 
    
- Unterscheiden sich die kurzfristigen Eintragsbezeichner von den langfristigen Bezeichnern, wobei alle Flags festgelegt werden. 
    
Clients können eine kurzfristige Eintrags-ID des zweiten Typs identifizieren, indem Sie das **abFlags** -Element wie folgt untersuchen: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Einige Dienstanbieter löschen ein oder mehrere Flags, um kurzfristige Eintragsbezeichner mit höherer Gültigkeit zu erstellen. Die folgenden **abFlags** -Elemente stellen beispielsweise kurzfristige Eintragsbezeichner dar, die für mehrere Tage oder für mehrere Sitzungen verwendet werden können: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Clients können kurzfristige Eintrags-IDs schnell erfassen, verwenden und verwerfen. In den meisten Fällen können Sie auf die gleiche Weise wie langfristige Eintragsbezeichner verwendet werden. Sie können aus einer Tabelle abgerufen werden, an die **OpenEntry** -Methode übergeben und mit der **CompareEntryIDs** -Methode verglichen werden. Die einzige Ausnahme besteht darin, dass Sie nie von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode zurückgegeben werden. Die von getProps zurückgegebenen Eigenschaften sind immer langfristige Eintragsbezeichner. **** 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Eintrags-IDs](mapi-entry-identifiers.md)

