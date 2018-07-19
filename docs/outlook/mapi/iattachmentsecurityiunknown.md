---
title: "\"IAttachmentSecurity\" IUnknown"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792014"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="9f7ee-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f7ee-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="9f7ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f7ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f7ee-105">Können Microsoft Outlook 2010 und Microsoft Outlook 2013-Lösungen zu ermitteln, ob die Anlage unsichere und zum Anzeigen und Indizierung blockierte betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f7ee-106">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="9f7ee-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9f7ee-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="9f7ee-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9f7ee-108">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="9f7ee-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9f7ee-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="9f7ee-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="9f7ee-110">Überprüft, ob eine angegebene Anlage zum Anzeigen und Indizieren von Outlook 2010 oder Outlook 2013 ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f7ee-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f7ee-111">Remarks</span></span>

<span data-ttu-id="9f7ee-112">Outlook 2010 und Outlook 2013-Lösungen können Abfragen diese Schnittstelle, um festzustellen, ob eine Anlage ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="9f7ee-113">Die Anlagen, die von Outlook 2010 oder Outlook 2013 blockiert werden variieren je nach wie Outlook 2010 oder Outlook 2013 konfiguriert wurde und die Richtlinien, die ein Administrator angewendet hat.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f7ee-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f7ee-114">See also</span></span>



[<span data-ttu-id="9f7ee-115">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9f7ee-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9f7ee-116">Überprüfen, ob eine Anlage blockiert ist</span><span class="sxs-lookup"><span data-stu-id="9f7ee-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

