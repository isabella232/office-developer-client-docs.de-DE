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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424553"
---
# <a name="saving-frequently-used-properties"></a>Speichern häufig verwendeter Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verbessern Sie die Leistung, indem Sie Daten speichern, die Zeit und Ressourcen zum Abrufen benötigten und häufig aufgerufen werden. Die Verwendung von zusätzlichem Arbeitsspeicher kann manchmal eine bessere Option sein, wenn wiederholte Abrufe verwendet werden. Verwenden Sie beim Erstellen eines Caches zum Speichern dieser Daten Vorsicht und Vorsicht. Beachten Sie, dass sich ein schlecht entworfener Cache negativ auf die Leistung auswirken kann.
  
Die meisten clients interpersonal message (IPM) müssen z. B. die IPM-Unterstruktur von Ordnern während einer typischen Sitzung mehrmals anzeigen und öffnen. Sie können die Leistung verbessern, indem Sie die Eintragsbezeichner für jeden dieser Ordner speichern. 
  

