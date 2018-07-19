---
title: Löschen eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a3006b43eb9f210603ff3a3d890118e7fd61d7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791514"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="74f97-103">Löschen eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="74f97-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="74f97-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74f97-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="74f97-105">**So entfernen einen oder mehrere Einträge im Adressbuch aus einem Container geändert werden**</span><span class="sxs-lookup"><span data-stu-id="74f97-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="74f97-106">Rufen Sie die [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) -Methode übergeben ein Array von Eintragsbezeichner, die zu löschenden Adressbucheinträge darstellen.</span><span class="sxs-lookup"><span data-stu-id="74f97-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="74f97-107">**DeleteEntries** kann eine Warnung MAPI_W_PARTIAL_COMPLETION, um anzugeben, dass sie eine oder mehrere Einträge löschen konnte nicht zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="74f97-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="74f97-108">Für diesen Rückgabewert mit dem Makro **HR_FAILED** testen Sie, und rufen Sie den Container [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode, wenn weitere Informationen zu dem Problem benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="74f97-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="74f97-109">Wenn Sie einen Zeiger auf einen gelöschten Eintrag [ADRENTRY](adrentry.md) -Struktur in den Cache gespeichert werden, werden Sie dennoch zum Abrufen von Eigenschaften mithilfe des Bezeichners Eintrag sein.</span><span class="sxs-lookup"><span data-stu-id="74f97-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="74f97-110">Dies ist, da der Eintrag nur zum Löschen markiert ist.</span><span class="sxs-lookup"><span data-stu-id="74f97-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="74f97-111">MAPI verwaltet eine Zugriffsebene für diese markierte Einträge Verhalten ist erwünscht.</span><span class="sxs-lookup"><span data-stu-id="74f97-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

