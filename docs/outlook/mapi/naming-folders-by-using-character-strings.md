---
title: Benennen von Ordnern mit Zeichenfolgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326250"
---
# <a name="naming-folders-by-using-character-strings"></a>Benennen von Ordnern mit Zeichenfolgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie während einer Sitzung häufig auf einen oder mehrere Ordner zugreifen, können Sie den Ordnern mit der [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) -Methode Namen zuweisen. Obwohl **IMsgStore:: SetReceiveFolder** hauptsächlich zum Erstellen spezieller Ordner zum Empfangen eingehender Nachrichten für bestimmte Nachrichtenklassen verwendet wird, kann Sie auch verwendet werden, um einen Ordner mit einem Namen zu verknüpfen. Der Name kann mit der Nachrichtenklasse identisch sein, oder es kann sich um eine beliebige Zeichenfolge handeln, die für die Verwendung durch den Client angepasst wurde. Das Zuordnen eines Namens zu einem Ordner verringert die Zeit, die zum Suchen und Öffnen des Ordners benötigt wird. 
  

