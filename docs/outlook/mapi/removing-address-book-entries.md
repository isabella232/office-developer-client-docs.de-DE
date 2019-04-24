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
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328350"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="3161f-103">Entfernen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="3161f-103">Removing address book entries</span></span>
  
<span data-ttu-id="3161f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3161f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3161f-105">Die [IABContainer::D eleteentries](iabcontainer-deleteentries.md) -Methode des Containers wird aufgerufen, um einen oder mehrere Empfänger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3161f-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="3161f-106">**DeleteEntries** hat zwei Parameter: ein Array von Eintrags Bezeichnern, die die zu löschenden Empfänger und einen reservierten Flags-Wert darstellen.</span><span class="sxs-lookup"><span data-stu-id="3161f-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="3161f-107">Das Löschen eines Empfängers wirkt sich auf die Inhaltstabelle ihres Containers aus; Zusätzlich zum Löschen des Empfängers muss der Container die Inhaltstabellen Zeile löschen, die den Empfänger darstellt.</span><span class="sxs-lookup"><span data-stu-id="3161f-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="3161f-108">Wenn die Zeile aus der Tabelle entfernt wurde, muss Ihr Container eine Tabellenbenachrichtigung für jeden registrierten Client ausgeben.</span><span class="sxs-lookup"><span data-stu-id="3161f-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="3161f-109">So implementieren Sie IABContainer::D eleteEntries</span><span class="sxs-lookup"><span data-stu-id="3161f-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="3161f-110">Löschen Sie jeden durch die Eintrags-ID dargestellten Empfänger aus Ihrem Container.</span><span class="sxs-lookup"><span data-stu-id="3161f-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="3161f-111">Wenn die Tabelle Inhalt Ihres Containers geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="3161f-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="3161f-112">Senden Sie eine _fnevTableModified_ -Benachrichtigung mit dem **ulTableEvent** -Element, das auf TABLE_ROW_DELETED für jede gelöschte Inhaltstabellen Zeile auf registrierte Clients festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3161f-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="3161f-113">Wenn Ihr Anbieter das Benachrichtigungs Dienstprogramm verwendet, rufen Sie [IMAPISupport:: notify](imapisupport-notify.md) auf, um diese Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="3161f-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="3161f-114">Wenn Ihr Anbieterobjekt Benachrichtigungen unterstützt, senden Sie auch eine _fnevObjectDeleted_ -Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3161f-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

