---
title: IAttachmentSecurity IUnknown
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
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411414"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="8cc63-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8cc63-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="8cc63-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cc63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cc63-105">Ermöglicht Microsoft Outlook 2010 und Microsoft Outlook 2013-Lösungen herauszufinden, ob eine Anlage als unsicher gilt und zum Anzeigen und Indizierung gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="8cc63-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8cc63-106">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="8cc63-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8cc63-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="8cc63-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8cc63-108">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="8cc63-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8cc63-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="8cc63-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="8cc63-110">Überprüft, ob eine angegebene Anlage von Outlook 2010 oder Outlook 2013 zur Anzeige und Indizierung blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="8cc63-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cc63-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8cc63-111">Remarks</span></span>

<span data-ttu-id="8cc63-112">Outlook 2010- und Outlook 2013-Lösungen können diese Schnittstelle abfragen, um zu sehen, ob eine Anlage blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="8cc63-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="8cc63-113">Die von Outlook 2010 oder Outlook 2013 blockierten Anlagen hängen davon ab, wie Outlook 2010 oder Outlook 2013 konfiguriert wurde und welche Richtlinien ein Administrator angewendet hat.</span><span class="sxs-lookup"><span data-stu-id="8cc63-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8cc63-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cc63-114">See also</span></span>



[<span data-ttu-id="8cc63-115">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="8cc63-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8cc63-116">Überprüfen, ob eine Anlage blockiert ist</span><span class="sxs-lookup"><span data-stu-id="8cc63-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

