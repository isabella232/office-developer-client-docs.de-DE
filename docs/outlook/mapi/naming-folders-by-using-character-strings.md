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
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="64479-103">Benennen von Ordnern mit Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="64479-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="64479-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64479-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64479-105">Wenn Sie einen oder mehrere Ordner während einer Sitzung häufig zugreifen, sollten Sie zum Zuweisen von Namen in die Ordner mit der [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="64479-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="64479-106">Obwohl **IMsgStore::SetReceiveFolder** in erster Linie herstellen Spezialordner Empfang eingehende Nachrichten für bestimmte Nachrichtenklassen verwendet wird, kann sie auch ein beliebiger Ordner mit einem Namen zuordnen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64479-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="64479-107">Der Name kann die Nachrichtenklasse identisch sein, oder es kann eine beliebige Zeichenfolge, die für die Verwendung des Clients angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="64479-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="64479-108">Zuordnen eines Namens zu einem Ordner verringert den Zeitaufwand zum Suchen und öffnen Sie den Ordner.</span><span class="sxs-lookup"><span data-stu-id="64479-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

