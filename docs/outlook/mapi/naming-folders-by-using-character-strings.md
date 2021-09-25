---
title: Benennen von Ordnern mithilfe von Zeichenzeichenfolgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 23fb125218923f823593c8d40694eb1337366289
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556021"
---
# <a name="naming-folders-by-using-character-strings"></a>Benennen von Ordnern mithilfe von Zeichenzeichenfolgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie während einer Sitzung häufig auf einen oder mehrere Ordner zugreifen, können Sie den Ordnern mit der [IMsgStore::SetReceiveFolder-Methode](imsgstore-setreceivefolder.md) Namen zuweisen. **Obwohl IMsgStore::SetReceiveFolder** hauptsächlich verwendet wird, um spezielle Ordner für den Empfang eingehender Nachrichten für bestimmte Nachrichtenklassen einzurichten, kann er auch verwendet werden, um einen beliebigen Ordner einem Namen zuzuordnen. Der Name kann mit der Nachrichtenklasse übereinstimmen oder eine beliebige Zeichenzeichenfolge sein, die für die Verwendung durch Den Client angepasst wurde. Das Zuordnen eines Namens zu einem Ordner verringert die Zeit, die zum Suchen und Öffnen des Ordners benötigt wird. 
  

