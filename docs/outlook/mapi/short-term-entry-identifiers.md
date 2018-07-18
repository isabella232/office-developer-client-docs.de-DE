---
title: Kurzfristige-Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f601971e61eb6430bef9d50b093642ee04b14044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795534"
---
# <a name="short-term-entry-identifiers"></a>Kurzfristige-Eintragsbezeichner

**Betrifft**: Outlook 
  
Kurzfristige Eintrags-ID wird von einem Dienstanbieter zu einem Objekt zugewiesen, wenn der Bezeichner schnell erstellt werden muss und muss nicht über die Zeit oder Abstand letzten. Die Eindeutigkeit von kurzfristige Eintrags-ID ist nur während der Lebensdauer der aktuellen Sitzung auf der aktuellen Arbeitsstation garantiert. In der Regel ist eine kurzfristige Eintrags-ID gültig nur, bis das Objekt, das es darstellt freigegeben wird. 
  
Kurzfristige-Eintragsbezeichner zugewiesenen auf Zeilen in Tabellen und den Einträgen in Dialogfeldern, in dem sie Daten zum Durchsuchen von schnell bereitstellen benötigt wird. Beispielsweise weisen Nachricht Anbieter kurzfristige-Eintragsbezeichner an Zeilen von Nachrichten in einer Inhaltstabelle und Empfänger in einer Empfängertabelle. 

Clients können diese kurzfristige-Eintragsbezeichner verwenden, um die Zeilen der Tabelle dargestellte Objekte zu öffnen. Im Gegensatz zu langfristige Eintragsbezeichner, die mit einer der Methoden **OpenEntry** verwendet werden können, sollte kurzfristige-Eintragsbezeichner mit dem Container **OpenEntry** -Methode verwendet werden. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implementieren von kurzfristige-Eintragsbezeichner

Die am häufigsten verwendeten Methoden, um kurzfristige-Eintragsbezeichner implementieren umfassen Folgendes:
  
- Stellt die kurzfristige-Eintragsbezeichner dieselbe wie die langfristige Bezeichner, wobei alle Kennzeichen nicht festgelegt. 
    
- Stellt die kurzfristige-Eintragsbezeichner langfristige-IDs festlegen aller die Kennzeichen anders. 
    
Clients können einen kurzfristigen Eintrag Bezeichner des zweiten Typs identifiziert, anhand dessen **AbFlags** Member wie folgt: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Einige Dienstanbieter deaktivieren Sie ein oder mehrere Flags zum kurzfristige-Eintragsbezeichner erstellen, die größer Gültigkeit haben. Die folgenden **AbFlags** Elemente darstellen beispielsweise kurzfristige Eintragsbezeichner, die für mehrere Tage oder mehrerer Sitzungen verwendet werden können: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Clients schnell zu erwerben, verwenden und kurzfristige-Eintragsbezeichner verwerfen. In den meisten Fällen können sie die gleiche Weise wie langfristige-Eintragsbezeichner verwendet werden. Sie können aus einer Tabelle, die **OpenEntry** -Methode übergeben, und im Vergleich mit **dem Eintragsbezeichner** abgerufen werden. Die einzige Ausnahme ist, dass sie nie aus der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zurückgegeben werden. Die Eigenschaften von **GetProps** zurückgegeben werden immer langfristige-Eintragsbezeichner. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

