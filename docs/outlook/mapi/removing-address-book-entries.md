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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425260"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="3113d-103">Entfernen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="3113d-103">Removing address book entries</span></span>
  
<span data-ttu-id="3113d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3113d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3113d-105">Die [IABContainer::D eleteEntries-Methode Ihres Containers](iabcontainer-deleteentries.md) wird aufgerufen, um einen oder mehrere Empfänger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3113d-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="3113d-106">**DeleteEntries** verfügt über zwei Parameter: ein Array von Eintragsbezeichnern, die die zu löschenden Empfänger darstellen, und einen reservierten Flagswert.</span><span class="sxs-lookup"><span data-stu-id="3113d-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="3113d-107">Das Löschen eines Empfängers wirkt sich auf das Inhaltsverzeichnis Des Containers aus. Zusätzlich zum Löschen des Empfängers muss ihr Container die Inhaltsverzeichniszeile löschen, die den Empfänger darstellt.</span><span class="sxs-lookup"><span data-stu-id="3113d-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="3113d-108">Wenn die Zeile aus der Tabelle entfernt wurde, muss ihr Container eine Tabellenbenachrichtigung an jeden registrierten Client aus senden.</span><span class="sxs-lookup"><span data-stu-id="3113d-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="3113d-109">So implementieren Sie IABContainer::D eleteEntries</span><span class="sxs-lookup"><span data-stu-id="3113d-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="3113d-110">Löschen Sie jeden Empfänger, der durch die Eintrags-ID dargestellt wird, aus Ihrem Container.</span><span class="sxs-lookup"><span data-stu-id="3113d-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="3113d-111">Wenn die Inhaltstabelle Ihres Containers geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="3113d-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="3113d-112">Senden Sie  _eine fnevTableModified-Benachrichtigung,_ bei der das **ulTableEvent-Element** auf TABLE_ROW_DELETED für jede gelöschte Inhaltstabellenzeile an registrierte Clients gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3113d-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="3113d-113">Wenn Ihr Anbieter das Benachrichtigungsprogramm verwendet, rufen [Sie IMAPISupport::Notify auf,](imapisupport-notify.md) um diese Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="3113d-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="3113d-114">Wenn Ihr Anbieter Objektbenachrichtigungen unterstützt, senden Sie auch eine _fnevObjectDeleted-Benachrichtigung._</span><span class="sxs-lookup"><span data-stu-id="3113d-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

