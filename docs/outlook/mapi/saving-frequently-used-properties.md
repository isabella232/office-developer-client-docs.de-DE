---
title: Speichern häufig verwendeter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 66dc993df65a12e0e3bc9ff22b043ba0e97b8471
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550141"
---
# <a name="saving-frequently-used-properties"></a>Speichern häufig verwendeter Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verbessern Sie die Leistung, indem Sie Daten speichern, die zeit- und ressourcenaufwendbar sind und häufig aufgerufen werden. Die Verwendung von zusätzlichem Arbeitsspeicher kann manchmal eine bessere Option für wiederholte Abrufe sein. Seien Sie vorsichtig, wenn Sie einen Cache zum Speichern dieser Daten erstellen. Bedenken Sie, dass sich ein schlecht entworfener Cache negativ auf die Leistung auswirken kann.
  
Beispielsweise müssen die meisten Interpersonal Message (IPM)-Clients die IPM-Unterstruktur von Ordnern während einer typischen Sitzung mehrmals anzeigen und öffnen. Sie können die Leistung verbessern, indem Sie die Eintragsbezeichner für jeden dieser Ordner speichern. 
  

