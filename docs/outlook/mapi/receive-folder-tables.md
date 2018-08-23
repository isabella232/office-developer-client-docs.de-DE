---
title: Tabellen für Empfängerordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573180"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="4ae0c-103">Tabellen für Empfängerordner</span><span class="sxs-lookup"><span data-stu-id="4ae0c-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="4ae0c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ae0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ae0c-105">Eine empfangen Ordner-Tabelle enthält Informationen für alle Ordner, die als Ordner für einen Nachrichtenspeicher empfangen.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="4ae0c-106">Eine Empfangsordner ist ein Ordner, in dem eingehende Nachrichten von einer bestimmten Nachrichtenklasse platziert werden.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="4ae0c-107">Store-implementierte Nachricht empfangen Ordner Tabellen, und Clientanwendungen von Anrufen an die [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="4ae0c-108">Die folgenden Eigenschaften bilden die erforderliche Spalte legen Sie im Ordner Tabellen zu empfangen:</span><span class="sxs-lookup"><span data-stu-id="4ae0c-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="4ae0c-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4ae0c-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="4ae0c-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4ae0c-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="4ae0c-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4ae0c-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ae0c-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ae0c-112">See also</span></span>



[<span data-ttu-id="4ae0c-113">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="4ae0c-113">MAPI Tables</span></span>](mapi-tables.md)

