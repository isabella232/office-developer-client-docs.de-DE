---
title: Entfernen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c5d7a2114f4a85b9f63cd778e899a83d335ff45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581279"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="83e42-103">Entfernen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="83e42-103">Removing address book entries</span></span>
  
<span data-ttu-id="83e42-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83e42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83e42-105">Des Containers [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) -Methode aufgerufen, um einen oder mehrere Empfänger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="83e42-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="83e42-106">**DeleteEntries** hat zwei Parameter: ein Array von Eintragsbezeichner, die die Empfänger zu löschenden darstellt und ein Flagwert reserviert.</span><span class="sxs-lookup"><span data-stu-id="83e42-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="83e42-107">Löschen eines Empfängers wirkt sich aus die Inhaltstabelle des Containers. Zusätzlich zu den Empfänger löschen, muss der Container für die Tabellenzeile Inhalt löschen, die den Empfänger darstellt.</span><span class="sxs-lookup"><span data-stu-id="83e42-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="83e42-108">Wenn die Zeile aus der Tabelle entfernt wurde, muss der Container für eine Benachrichtigung über eine Tabelle auf allen registrierten Clients ausstellen.</span><span class="sxs-lookup"><span data-stu-id="83e42-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="83e42-109">Implementieren von IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="83e42-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="83e42-110">Löschen Sie jeden Empfänger, dargestellt durch die Eintrags-ID aus dem Container.</span><span class="sxs-lookup"><span data-stu-id="83e42-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="83e42-111">Wenn Inhaltstabelle des Containers geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="83e42-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="83e42-112">Senden Sie eine Benachrichtigung _FnevTableModified_ mit dem **UlTableEvent** -Element festlegen, um den registrierten Clients für jede Tabellenzeile gelöschten Inhalt TABLE_ROW_DELETED.</span><span class="sxs-lookup"><span data-stu-id="83e42-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="83e42-113">Wenn der Anbieter das Dienstprogramm Benachrichtigung verwendet wird, rufen Sie [IMAPISupport::Notify](imapisupport-notify.md) , um diese Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="83e42-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="83e42-114">Wenn der Anbieter Objekt Benachrichtigungen unterstützt, auch senden Sie eine _FnevObjectDeleted_ -Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="83e42-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

