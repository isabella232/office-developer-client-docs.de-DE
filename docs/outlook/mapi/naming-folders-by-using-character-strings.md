---
title: Benennen von Ordnern mithilfe von Zeichenfolgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793285"
---
# <a name="naming-folders-by-using-character-strings"></a>Benennen von Ordnern mithilfe von Zeichenfolgen

  
  
**Betrifft**: Outlook 
  
Wenn Sie einen oder mehrere Ordner während einer Sitzung häufig zugreifen, sollten Sie zum Zuweisen von Namen in die Ordner mit der [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) -Methode. Obwohl **IMsgStore::SetReceiveFolder** in erster Linie herstellen Spezialordner Empfang eingehende Nachrichten für bestimmte Nachrichtenklassen verwendet wird, kann sie auch ein beliebiger Ordner mit einem Namen zuordnen verwendet werden. Der Name kann die Nachrichtenklasse identisch sein, oder es kann eine beliebige Zeichenfolge, die für die Verwendung des Clients angepasst werden. Zuordnen eines Namens zu einem Ordner verringert den Zeitaufwand zum Suchen und öffnen Sie den Ordner. 
  

