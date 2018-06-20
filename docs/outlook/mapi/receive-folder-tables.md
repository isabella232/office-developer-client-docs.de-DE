---
title: Ordner Tabellen empfangen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f3bcda3beb29fa91629ea1639522ef24dc6eb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795347"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="9818f-103">Ordner Tabellen empfangen</span><span class="sxs-lookup"><span data-stu-id="9818f-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="9818f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9818f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9818f-105">Eine empfangen Ordner-Tabelle enthält Informationen für alle Ordner, die als Ordner für einen Nachrichtenspeicher empfangen.</span><span class="sxs-lookup"><span data-stu-id="9818f-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="9818f-106">Eine Empfangsordner ist ein Ordner, in dem eingehende Nachrichten von einer bestimmten Nachrichtenklasse platziert werden.</span><span class="sxs-lookup"><span data-stu-id="9818f-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="9818f-107">Store-implementierte Nachricht empfangen Ordner Tabellen, und Clientanwendungen von Anrufen an die [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="9818f-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="9818f-108">Die folgenden Eigenschaften bilden die erforderliche Spalte legen Sie im Ordner Tabellen zu empfangen:</span><span class="sxs-lookup"><span data-stu-id="9818f-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="9818f-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9818f-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="9818f-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9818f-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="9818f-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9818f-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9818f-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9818f-112">See also</span></span>



[<span data-ttu-id="9818f-113">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="9818f-113">MAPI Tables</span></span>](mapi-tables.md)

