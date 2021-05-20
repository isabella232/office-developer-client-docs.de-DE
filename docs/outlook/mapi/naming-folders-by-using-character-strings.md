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
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="e96f5-103">Benennen von Ordnern mithilfe von Zeichenzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="e96f5-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="e96f5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e96f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e96f5-105">Wenn Sie während einer Sitzung häufig auf einen oder mehrere Ordner zugreifen, sollten Sie den Ordnern mit der [IMsgStore::SetReceiveFolder-Methode Namen](imsgstore-setreceivefolder.md) zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e96f5-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="e96f5-106">Obwohl **IMsgStore::SetReceiveFolder** hauptsächlich zum Einrichten spezieller Ordner zum Empfangen eingehender Nachrichten für bestimmte Nachrichtenklassen verwendet wird, kann es auch verwendet werden, um einen beliebigen Ordner einem Namen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e96f5-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="e96f5-107">Der Name kann mit der Nachrichtenklasse identisch sein, oder er kann eine beliebige Zeichenzeichenfolge sein, die für die Verwendung Ihres Clients angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="e96f5-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="e96f5-108">Das Zuordnen eines Namens zu einem Ordner verringert die Zeit, die zum Suchen und Öffnen des Ordners benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e96f5-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

