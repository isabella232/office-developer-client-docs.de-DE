---
title: Benennen von Ordnern mithilfe von Zeichenzeichenfolgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428312"
---
# <a name="naming-folders-by-using-character-strings"></a>Benennen von Ordnern mithilfe von Zeichenzeichenfolgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie während einer Sitzung häufig auf einen oder mehrere Ordner zugreifen, sollten Sie den Ordnern mit der [IMsgStore::SetReceiveFolder-Methode Namen](imsgstore-setreceivefolder.md) zuweisen. Obwohl **IMsgStore::SetReceiveFolder** hauptsächlich zum Einrichten spezieller Ordner zum Empfangen eingehender Nachrichten für bestimmte Nachrichtenklassen verwendet wird, kann es auch verwendet werden, um einen beliebigen Ordner einem Namen zuzuordnen. Der Name kann mit der Nachrichtenklasse identisch sein, oder er kann eine beliebige Zeichenzeichenfolge sein, die für die Verwendung Ihres Clients angepasst wurde. Das Zuordnen eines Namens zu einem Ordner verringert die Zeit, die zum Suchen und Öffnen des Ordners benötigt wird. 
  

