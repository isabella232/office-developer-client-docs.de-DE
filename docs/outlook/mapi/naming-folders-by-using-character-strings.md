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
ms.openlocfilehash: 93d959bf41b5d18610d77c6b5573895b0e3880d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594586"
---
# <a name="naming-folders-by-using-character-strings"></a>Benennen von Ordnern mit Zeichenfolgen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn Sie einen oder mehrere Ordner während einer Sitzung häufig zugreifen, sollten Sie zum Zuweisen von Namen in die Ordner mit der [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) -Methode. Obwohl **IMsgStore::SetReceiveFolder** in erster Linie herstellen Spezialordner Empfang eingehende Nachrichten für bestimmte Nachrichtenklassen verwendet wird, kann sie auch ein beliebiger Ordner mit einem Namen zuordnen verwendet werden. Der Name kann die Nachrichtenklasse identisch sein, oder es kann eine beliebige Zeichenfolge, die für die Verwendung des Clients angepasst werden. Zuordnen eines Namens zu einem Ordner verringert den Zeitaufwand zum Suchen und öffnen Sie den Ordner. 
  

