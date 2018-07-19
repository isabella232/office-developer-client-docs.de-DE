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
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793285"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="244b2-103">Benennen von Ordnern mit Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="244b2-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="244b2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="244b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="244b2-105">Wenn Sie einen oder mehrere Ordner während einer Sitzung häufig zugreifen, sollten Sie zum Zuweisen von Namen in die Ordner mit der [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="244b2-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="244b2-106">Obwohl **IMsgStore::SetReceiveFolder** in erster Linie herstellen Spezialordner Empfang eingehende Nachrichten für bestimmte Nachrichtenklassen verwendet wird, kann sie auch ein beliebiger Ordner mit einem Namen zuordnen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="244b2-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="244b2-107">Der Name kann die Nachrichtenklasse identisch sein, oder es kann eine beliebige Zeichenfolge, die für die Verwendung des Clients angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="244b2-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="244b2-108">Zuordnen eines Namens zu einem Ordner verringert den Zeitaufwand zum Suchen und öffnen Sie den Ordner.</span><span class="sxs-lookup"><span data-stu-id="244b2-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

