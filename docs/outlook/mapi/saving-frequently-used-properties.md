---
title: Speichern häufig verwendeter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e32ed3388e95d32a4857a933fb735d170dd71688
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283107"
---
# <a name="saving-frequently-used-properties"></a>Speichern häufig verwendeter Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verbessern Sie die Leistung, indem Sie Daten speichern, die Zeit und Ressourcen zum Abrufen benötigen und häufig auf Sie zugegriffen wird. Die Verwendung von zusätzlichem Arbeitsspeicher kann manchmal eine bessere Option für wiederholte Abrufe sein. Verwenden Sie beim Erstellen eines Caches zum Speichern dieser Daten Vorsicht und Sorgfalt. Beachten Sie, dass ein schlecht entworfener Cache sich negativ auf die Leistung auswirken kann.
  
Beispielsweise müssen die meisten IPM-Clients (zwischen Personen) die IPM-Unterstruktur von Ordnern während einer typischen Sitzung mehrmals anzeigen und öffnen. Sie können die Leistung verbessern, indem Sie die Eintrags-IDs für jeden dieser Ordner speichern. 
  

