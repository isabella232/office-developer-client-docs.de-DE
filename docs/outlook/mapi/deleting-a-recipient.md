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
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421046"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="c44c7-103">Löschen eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="c44c7-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="c44c7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c44c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c44c7-105">**So entfernen Sie einen oder mehrere Adressbucheinträge aus einem veränderbaren Container**</span><span class="sxs-lookup"><span data-stu-id="c44c7-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="c44c7-106">Rufen Sie [die IABContainer::D eleteEntries-Methode](iabcontainer-deleteentries.md) auf, und übergeben Sie ein Array von Eintragsbezeichnern, die die zu löschenden Adressbucheinträge darstellen.</span><span class="sxs-lookup"><span data-stu-id="c44c7-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="c44c7-107">**DeleteEntries** kann eine Warnung MAPI_W_PARTIAL_COMPLETION, die angibt, dass ein oder mehrere Einträge nicht gelöscht werden konnten.</span><span class="sxs-lookup"><span data-stu-id="c44c7-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="c44c7-108">Testen Sie diesen Rückgabewert mit HR_FAILED **Makro,** und rufen Sie die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) des Containers auf, wenn weitere Informationen zum Problem erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c44c7-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="c44c7-109">Wenn Sie einen Zeiger auf die [ADRENTRY-Struktur](adrentry.md) eines gelöschten Eintrags in Ihrem Cache halten, können Sie eigenschaften weiterhin mithilfe des Eintragsbezeichners abrufen.</span><span class="sxs-lookup"><span data-stu-id="c44c7-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="c44c7-110">Dies liegt daran, dass der Eintrag nur zum Löschen markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c44c7-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="c44c7-111">MAPI behält eine Ebene des Zugriffs auf diese markierten Einträge nach Entwurf bei.</span><span class="sxs-lookup"><span data-stu-id="c44c7-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

