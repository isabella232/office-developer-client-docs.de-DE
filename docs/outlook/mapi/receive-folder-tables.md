---
title: Empfangen von Ordnertabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417350"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="50f5a-103">Empfangen von Ordnertabellen</span><span class="sxs-lookup"><span data-stu-id="50f5a-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="50f5a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50f5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50f5a-105">Eine Tabelle mit Empfangsordnern enthält Informationen zu allen Ordnern, die als Empfangsordner für einen Nachrichtenspeicher festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="50f5a-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="50f5a-106">Ein Empfangsordner ist ein Ordner, in dem eingehende Nachrichten einer bestimmten Nachrichtenklasse platziert werden.</span><span class="sxs-lookup"><span data-stu-id="50f5a-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="50f5a-107">Nachrichtenspeicheranbieter implementieren Empfangsordnertabellen, und Clientanwendungen verwenden sie, indem sie die [IMsgStore::GetReceiveFolderTable-Methode](imsgstore-getreceivefoldertable.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50f5a-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="50f5a-108">Die folgenden Eigenschaften stellen die erforderliche Spaltenmappe in den Tabellen des Empfangsordners zusammen:</span><span class="sxs-lookup"><span data-stu-id="50f5a-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="50f5a-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="50f5a-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="50f5a-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="50f5a-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="50f5a-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="50f5a-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50f5a-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50f5a-112">See also</span></span>



[<span data-ttu-id="50f5a-113">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="50f5a-113">MAPI Tables</span></span>](mapi-tables.md)

